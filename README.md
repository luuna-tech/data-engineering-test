# ZeBrands Data Engineering Test

Welcome! 

The following test is meant to give us a sense of your skills by presenting you with a simplified scenario similar to the kind of situations you'll face as a Data Engineer at ZeBrands.

Please read the instructions fully and carefully. Feel free to get in touch with your recruiter should you need further clarification.

## Important

- The test may feel ambiguous at points because we want you to feel obligated to make design decisions. In real life you will often find this to be the case.
- Do not feel discouraged if you don't know how to do something immediately. Learning quickly and figuring things out are valuable skills that are also being evaluated.
- Keep it honest. You may very well face a situation like this on your first day at ZeBrands, so while you should feel free to search the internet for help, having someone else complete the test for you benefits no one.
- Don't give up. Let us know if you need more time.
- Incomplete tests are still evaluated for partial credit.
- Please do not think of this as an exam but rather a demo for your skills in building an actual working product. We´re not looking for technical perfection or theoretical depth (although both are benefitial).

## Scenario

ZeBrands sends and evaluates surveys to it's customers using the [NPS framework](https://www.qualtrics.com/experience-management/customer/net-promoter-score/#:~:text=NPS%20stands%20for%20Net%20Promoter,of%20customers%20to%20a%20company.&text=Promoters%20respond%20with%20a%20score,score%20of%207%20or%208).

Our CEO needs visibility on what our customers think of our services and products from these surveys.

We want to quickly build a data tool that will help him visualize NPS categories from surveys by various date aggregations and gather other interesting insights from the survey scores (e.g score trends, averages, medians, etc).

Your goal is to build that tool by using whatever frameworks you feel most comfortable with. We want to see what you can do, so think of this as a showcase for what you can deliver and make something cool.

## Data

In order to pull the list of reviews and their corresponding dates, you will need to conect to a PostgresSQL instance:

```bash
user: candidate
password: goodluck
host: public.ck1z34lm7sx8.us-east-1.rds.amazonaws.com
```

Surveys are identified by a unique ID, and their timestamp is stored as a Unix timestamp. You will find only these two attributes in the database.

In order to pull the actual score for each Survey, you will need to query a REST endpoint located at:

```bash
https://dm1pddaxy1.execute-api.us-east-1.amazonaws.com/default/data-engineering-test-api
```

By calling the GET method on this endpoint and providing the survey_id attribute as an URL parameter, the server will respond with the score for each survey.

Example:

```bash
https://dm1pddaxy1.execute-api.us-east-1.amazonaws.com/default/data-engineering-test-api?survey_id=2000
```

Once you´ve figured out how you want to pull and join the data, the rest is up to you. These are some tools we find useful for these kind of tasks, but do not feel required to use them:

- [Shiny](https://shiny.rstudio.com/gallery/)
- [Bokeh](https://docs.bokeh.org/en/latest/docs/gallery.html)
- [Data Studio](https://marketingplatform.google.com/about/data-studio/gallery/)
- [Chart JS](https://www.chartjs.org/)



## Delivering your solution

Should you need to provision any specific resources to deliver or package your solution, let us know.

You can provide us with a link to your personal repository, email us the code with instructions on how to run it or whatever works best for you.

## Good luck

Email any questions to your recruiter or data@luuna.mx
