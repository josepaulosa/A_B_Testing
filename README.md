## **A/B Testing**<br>
> **Definition**: A/B testing is a way to compare two versions of something to find out which performs better. It is one of the simplest forms of a randomized controlled experiment.<br>

> **How it works**: the test works by showing to two groups of users (with equal or different number of partcipants), assigned at random, different versions of a product, drug, site, etc., and determining which version has most successful metrics (previously chosen according to the goals of the experiment. <br>

> **Technical characteristics**:
> - Randomized controlled experiment.
> - One version is the control and the other is the treatment. The treatment is a new version that we want to figure out if it performs better than the old one (in clinical trials the control can be a placebo).
> - One has to estimate the sample size to achieve statistical significance.
> - Blocking technique should be used whenever necessary as a means of accounting for certain biases that may be found in any group to maintain randomness in our sampling.<br>
- - - 
### Info on datasets:
You can find the dataset &rarr; [here](https://www.kaggle.com/datasets/zhangluyuan/ab-testing?select=ab_data.csv).
- The dataset contains information about almost 300K+ users that were involved in a A/B test. It is an **`unpaired`** dataset
- Features:
    - user_id: unique identifier for each user.
    - timestamp: associated date and time for each visit to the website by a given user.
    - group: the category a user was grouped into pre-A/B test (control or treatment groups).
    - landing_page: the page that was displayed to a user when they visited the company website (new_page or old_page).
    - converted: whether a user converted or not (0 or 1); Note: Users in the control group ought to be displayed the old page, while those in the treatment group ought to see the new page.
    - - - 
#### &rarr; In the notebook, besides performing an A/B test, I explain the `assumptions` and `hypothesis` of a `two proportions z-test`.
- - - 
### Aditional considerations:
- When performing an A/B test if one is testing just one feature, e.g., the size of the subscribe button, that is relatively simple test to perform. One might not be testing just the size but also the color, the text, the typeface, and the font size. If we run **`sequential tests`**, e.g., testing size first (large versus small), then testing color (blue versus red), then testing typeface (Times versus Arial), because we believe we shouldn’t vary two or more factors at the same time, these sequential tests are **`suboptimal`** because **`we’re not measuring what happens when factors interact`** (like, for instance, the **`interaction effects in linear regression`)**. For example, it may be that users prefer blue on average but prefer red when it’s combined with Arial. This kind of result is regularly missed in sequential A/B testing because the typeface test is run on blue buttons that have “won” the prior test.

- Instead, we should run more complex tests. Using mathematics we can pick and run **only certain subsets of those treatments**; then we can **infer the rest from the data**. This is called **`multivariate testing`** in the A/B testing world and often means we end up doing an **`A/B/C test`** or even an **`A/B/C/D test`**. In the example above with colors and size, it might mean showing different groups: a large red button, a small red button, a large blue button, and a small blue button. If wwe wanted to test fonts too, the number of test groups would grow even more.
