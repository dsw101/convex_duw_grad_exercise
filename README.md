# Should we underwrite this binder?

You are a delegated property underwriter at Convex

You have just been presented with a **huge** opportunity:

A big UK insurer, "OmniInsure UK" has offered you to underwrite the flood covers for their home buildings insurance 
portfolio.

Convex will take the premiums, and pay the claims.

Should we do it?

## Things you should know

In insurance we talk about loss ratio - which is the sum of claims divided by the sum of premium

In order to be profitable, we need a loss ratio of 60% or lower.

We can measure the loss ratio for a "year of policies" (i.e. 2025 or 2024) - which tells us how profitable each year was

But we know that flood insurance loss ratios are volatile from year to year, depending on whether there is a big 
flood event

So what we really need is a statistical **expected** loss ratio next year of 60% or lower, taking into account the range
of possible events

## The data

You have been provided with two data sets:

1. ```policies_and_claims.parquet```: one row for each policy written by OmniInsure years 2021 through 2025. There
is one row per policy per year. Cost of claims is also shown.

2. ```uk_industry_wide_annual_losses.parquet```: UK Industry wide data for flood claims, per year, from 2000 through 2025.

We have also given you a little notebook to get you started understanding the data (src/solution/getting_started.ipynb)

## The rules

 - Please **don't spend more than a couple of hours on this** (we know you're busy!). There will be "more you could look at" if you had time - but that's fine!
 - To save time, please feel free to use Claude / Gemini / CoPilot or your LLM of choice (our favourite at the moment is Claude)
 - We don't need you to be precise or actuarial -- just show us that you have understood some of the dynamics and
 have a good brain... The answer doesn't require precision!
  - Please be ready to talk an imaginary underwriter through your answer 

## Some things to be aware of

 - In the premium and claims data, you will find a couple of "rating factors" columns: ```Excess``` and ```Geographic Flood Risk```.
 Geographic Flood Risk is based on the address of the house, looked up on our in house "flood risk" map - which shows the level of flood risk at each geographic location.

 - ```Sum Insured``` is the expected rebuild cost of the building. We call it the "exposure measure", because, all other things being equal, expected claims cost of a building, or of a whole portfolio, is roughly proportional to this measure. (Of course, if the building or portfolio mix is higher or lower geographic risk the expected claims cost will be higher or lower)