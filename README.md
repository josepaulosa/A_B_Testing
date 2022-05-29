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
- The dataset contains information about almost 300K+ users that were involved in a A/B test. It is an `unpaired` dataset
- Features:
    - user_id: unique identifier for each user.
    - timestamp: associated date and time for each visit to the website by a given user.
    - group: the category a user was grouped into pre-A/B test (control or treatment groups).
    - landing_page: the page that was displayed to a user when they visited the company website (new_page or old_page).
    - converted: whether a user converted or not (0 or 1); Note: Users in the control group ought to be displayed the old page, while those in the treatment group ought to see the new page.
    - - - 
#### &rarr; In the notebook, besides performing an A/B test, I explain the `assumptions` and `hypothesis` of a `two proportion z-test`.
- - - 
### Aditional considerations:
- ppp
