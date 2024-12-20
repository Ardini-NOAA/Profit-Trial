# The Use of Cost Survey Data to Calculate Vessel Profits for Commercial Fishing Fleets in the Northeast U.S.


# Introduction
Profit is an important metric in assessing the economic performance of commercial fishing fleets and in evaluating the impacts of proposed regulations. Evaluation of economic impacts is required under a number of laws, including Including the Magnuson-Stevens Fishery Conservation and Management Act (MSA), the National Environmental Policy Act (NEPA), Executive Order 12866, and the Regulatory Flexibility Act (RFA). 

Within the Northeast United States, commercial revenues are readily available to NOAA Fisheries, as all federally permitted vessels are required to report sales to licensed dealers. Cost data, on the other hand, have generally been the limiting factor in calculating vessel profits. The Northeast Fisheries Science Center conducts a voluntary survey to collect comprehensive cost information from commercial fishing vessel owners. This survey was last implemented during 2023 for costs incurred during calendar year 2022. One of the primary goals of the survey was to calculate vessel-level profits. 

Using data primarily collected from the most recent cost survey, this site presents commercial fishing vessel profits during 2022 for those vessels who participated in the survey effort. All information presented follows data confidentiality rules as required under the MSA (at least 3 vessels must be present in each summary group). These snapshots will serve as a performance metric in evaluating the economic impacts of proposed fishery management actions. 


# Cost Survey Background
Starting in 2007, the Social Sciences Branch (SSB) of the Northeast Fisheries Science Center (NEFSC) has intermittently collected commercial fishing cost information from vessel owners through a voluntary survey. The most recent survey, formally known as the Greater Atlantic Region Commercial Fishing Business Cost Survey for 2022 (hereafter 2022 cost survey), was fielded in March-August 2023 to collect costs incurred by vessel owners during calendar year 2022. The 2022 cost survey was split up into the following sections:

General Information
New/Replacement, Repair/Maintenance, Upgrade and Other Costs for the Selected Vessel
Trip Expenses for the Selected Vessel
Crew Payment System for the Selected Vessel
Overhead Costs
The Value of the Selected Vessel
Quota Costs and Revenues for the Selected Vessel
Completeness of Cost Information
Survey Follow-up Questions

Each owner of a federally permitted commercial fishing vessel that was active in either calendar year 2021 or 2022 received a survey. A total of 2,495 individuals were sent the 2022 cost survey with 422 surveys returned. After accounting for incomplete returned surveys and ineligibles within the sampling frame, the final response rate was 15.0% (371/2,477). For further details on the implementation of the 2022 cost survey see Werner et al. (2025). For more information on early iterations of the cost survey, see Das (2015) and Ardini et al. (2022).


# Metrics
There are a number of different metrics to measure net returns to commercial fishing businesses as detailed in Kitts et al. (2022). For example a cash flow statement typically shows returns over time and can help inform the need to acquire cash reserves through loans. An income statement is somewhat similar to a cash flow statement and focuses on gross revenues and costs associated with operating a fishing business. An economic profit statement includes opportunity costs, such as physical capital costs and the vessel owner’s time. A vessel may yield a positive accounting profit but a negative economic profit after accounting for opportunity costs.

This page provides modified income statements looking at both operating profit and total profit. Operating profit can help inform the immediate viability of a fishing business- if trip expenses cannot be covered, economic theory suggests that the vessel will cease operations. Total profit measured over an extended time period informs the long-term viability of a fishing business. Measured for 2022, this metric can be used to calculate profit margin, the ratio of profit to gross revenues. However, a negative total profit for 2022 does not necessarily translate into a fishing business that is not viable as some costs, such as vessel repairs, are expected to fluctuate from year to year.

## Operating Profit
Operating profit refers to gross revenues minus operating costs (variable costs). Within the 2022 cost survey, two sections in particular cover operating costs. The trip expenses section (#3) collects information on fuel, bait, ice, and food. The crew payment section (#4) includes the total amount paid to crew and hired captains, as well as any benefits paid out. Outside of the survey, a few costs collected by at-sea observers, fresh water and crew supplies, are also included in the operating profit calculation.

## Total Profit
Total profit refers to operating profit minus non-operating costs (fixed and quasi-fixed costs). Within the 2022 cost survey, a few different sections include non-operating costs. The vessel repairs, upgrades, and other costs section (#2) includes the amount spent on various vessel components including the engine, hull, fishing gear, electronics, and safety equipment. Other vessel costs such as mooring fees, permit fees, and vessel insurance are also included. The overhead section (#5) includes, among other costs, business vehicle expenses, association fees, non-crew labor payments, and office/storage expenses. The quota costs and revenue section (#7) is also included as a component of non-operating costs.


# Respondent Pool
A total of 422 surveys were returned to the Social Sciences Branch at the conclusion of the 2022 cost survey. Profit calculations were first performed for all observations followed by a series of steps to eliminate those observations that were deemed inappropriate to include.

## Filtering of Observations
The first filtering step specified that all surveys must have answered at least one cost-related question. This step eliminated 55 observations, bringing the total number to 367. The second filtering step specified that the responding vessel must be commercially active (revenues >$0) during 2022. A further 46 observations were dropped, bringing the total to 321.

Following completion of the initial filtering, a few other steps were performed. The 2022 cost survey included the nine sections listed under Cost Survey Background. For each response, the number of survey sections skipped were counted, where a skipped section was any case in which all questions within the section were left blank. For this exercise, five survey sections were evaluated. Sections 3-5 were evaluated in entirety while section 2 was divided into sub-sections of vessel repairs/upgrades questions and vessel fees/insurance questions. If a survey skipped multiple sections, it was removed from the dataset. A total of 17 observations skipped multiple survey sections, bringing the total to 304. An additional 12 observations out of the remaining 304 skipped one survey section. These cases were further evaluated to look at the specific section skipped. Four out of the 12 only skipped the crew payment section. Since these were all small vessels with relatively low costs and operating profit, assuming there was no crew on board was deemed appropriate. The other 8 observations that skipped one survey section were dropped, resulting in a final dataset of 296 observations. The number of survey questions answered for each observation in the final dataset are shown in Table 1.

questions_answered<- read.csv(file="V:/Ardini_Cost_Survey/SAS_Cost_Survey/Profitability_Profiles/Calculate_Profit/Final/questions_answered_final.csv")


# Profit Calculation Methods

## Commercial Revenue
All individuals that were sampled for the 2022 cost survey were owners of federally-permitted commercial fishing vessels active in 2021 or 2022. Federally-permitted vessels are required to sell their catch to federally-licensed seafood dealers and commercial revenue is derived from harvested catch on commercial trips sold to a licensed dealer. All vessels included in the profit snapshots generated commercial fishing revenue >$0 during 2022 from landings occurring in the Northeast region (ME to Cape Hatteras, NC). 

Vessel primary gear is defined according to the largest contributor to total commercial vessel revenue during 2022. Fishing gears, primarily from Vessel Trip Reports (VTRs) were grouped into the same categories as used for the 2022 cost survey sampling frame. For example, bottom trawl and midwater trawl were grouped into a broader trawl category. The resulting primary gear groups are as follows: gillnet, handgear, hydraulic dredge, longline, pot/trap, scallop dredge, seine, trawl, and unknown. Due to low response levels for some primary gear groups, results are unable to be presented.

Vessel primary fishery is also defined as the largest contributor to total commercial vessel revenue during 2022. Species were grouped into Fishery Management Plans (FMPs) as managed by the New England and Mid-Atlantic Fishery Management Councils, as well as American lobster, managed by the Atlantic States Marine Fisheries Commission. All other fisheries are grouped into “Other”. Due to low response levels for some primary fisheries, results are unable to be presented.

## For-Hire Revenue
While the 2022 cost survey was sent to vessels engaged in commercial fishing during 2021 or 2022, some of these vessels also were engaged in for-hire fishing. In order to most accurately capture vessel-level profits, it is important to include this additional source of revenue. For-hire revenue is derived from angler/customer payments on recreational trips.

All 2022 party/charter trips, and the number of anglers per trip, were first pulled from logbook data. Average angler charter/guide fees by state were then retrieved from the results of the 2022 National Angler Expenditure Survey administered by NOAA Fisheries. This survey is conducted every 3-5 years to better understand the economic contribution of recreational fishing within each region. The survey collects information on a variety of angler expenditures including bait, ice, lodging, and travel costs. For the purpose of the vessel profit calculation, only the amount paid by the angler for the party/charter ticket is used. State-level averages from the angler expenditure survey were used in light of the variability in fees by state within the Northeast region as well as the high level of response for each state. The average angler fee was multiplied by the number of anglers for each 2022 party/charter trip by state. Finally, the trip-level calculations were summed to an annual vessel-level value.

## Survey Costs
The vast majority of cost information used in the calculation of vessel profits came directly from the 2022 cost survey. Some manipulation of the data was required to make it usable at the vessel/annual level. These data manipulation steps are summarized below.

Operating Costs: Survey respondents were given the option of providing operating costs such as fuel, bait, and ice either at the annual level or as an average by trip. For those respondents who filled in the average cost by trip, the value was multiplied by the number of commercial trips taken during 2022. In general, the number of trips was used directly from the survey (Q2). In cases where this information was not filled in, the number of trips was retrieved from VTRs and/or dealer reports.

Overhead Costs: Survey respondents were given the option of providing these costs either at the vessel level or at the business level. For those respondents who filled in business level costs, the value was divided by the number of vessels owned by the respondent during 2022. The number of vessels owned was taken directly from the survey (Q13).

Quota Leasing Costs: Survey respondents were given the option to provide quota leasing costs either at the vessel-level or across multiple vessels. If this cost was provided across multiple vessels, the value was divided by the specific number of vessels the quota leasing cost was attributed to (Q17).

Other Costs: At the end of the survey, respondents were given the opportunity to list other costs that were not included in the survey. When other costs were listed, they were evaluated on a case-by-case basis (see Werner et al. 2025). Those that could not be allocated to an existing cost category were excluded from the profit calculation.

## Additional Trip Costs
As covered in the previous section, the 2022 cost survey queried a variety of expenses faced by vessel owners. During pre-testing of the survey instrument, fishing industry members generally felt that the survey did a good job of including all significant costs. Furthermore, comments on the survey itself and a lack of other costs filled in by respondents indicated the survey covered significant costs. However there are two costs, crew supplies and fresh water, that are collected by at-sea observers that were not included in the 2022 cost survey. 

To capture these costs, data from observer programs was used to calculate average costs per trip by gear. All 2022 trips from observer data tables were pulled, along with the primary gear utilized on each trip. The average crew supply and fresh water trip costs by gear type were calculated and these averages were then merged by gear with all of the trips taken by survey responding vessels during 2022. Finally, trip-level costs were summed to the vessel-level.


## Depreciation
The final cost component included in the profit calculation is vessel depreciation. Ideally, a different depreciation value would be assigned to each physical capital component (e.g. electronics, engine, hull) using the age of the equipment. This method would require additional information beyond that collected in the 2022 cost survey. 

Information on estimated market vessel value was collected in the 2022 cost survey, however responses to this question were lower than most other survey questions. The lower number of responses can be explained in part by the inclusion of a “I Prefer not to Answer” option, which  was not included for other survey questions. An alternate method was used to estimate vessel value by estimating shadow values of vessel characteristics- age, gross tonnage, length, and type of construction. A depreciation cost was applied to the vessel value at different rates depending on the age of the vessel. 


# Revenue Summary
gear_revenue<- read.csv(file="V:/Ardini_Cost_Survey/SAS_Cost_Survey/Profitability_Profiles/Calculate_Profit/Final/revenue_summary/gear_revenue_no_conf.csv")

fmp_revenue<- read.csv(file="V:/Ardini_Cost_Survey/SAS_Cost_Survey/Profitability_Profiles/Calculate_Profit/Final/revenue_summary/fmp_revenue_no_conf.csv")

gear_fmp_revenue<- read.csv(file="V:/Ardini_Cost_Survey/SAS_Cost_Survey/Profitability_Profiles/Calculate_Profit/Final/revenue_summary/gear_fmp_revenue_no_conf.csv")

# Cost Summary

gear_cost<- read.csv(file="V:/Ardini_Cost_Survey/SAS_Cost_Survey/Profitability_Profiles/Calculate_Profit/Final/cost_summary/gear_cost_no_conf.csv")

fmp_cost<- read.csv(file="V:/Ardini_Cost_Survey/SAS_Cost_Survey/Profitability_Profiles/Calculate_Profit/Final/cost_summary/fmp_cost_no_conf.csv")

gear_fmp_cost<- read.csv(file="V:/Ardini_Cost_Survey/SAS_Cost_Survey/Profitability_Profiles/Calculate_Profit/Final/cost_summary/gear_fmp_cost_no_conf.csv")

## Cost Distributions

gear_dist<- read.csv(file="V:/Ardini_Cost_Survey/SAS_Cost_Survey/Profitability_Profiles/Calculate_Profit/Final/cost_contributors/gear_cost_cat_perc.csv")

fmp_dist<- read.csv(file="V:/Ardini_Cost_Survey/SAS_Cost_Survey/Profitability_Profiles/Calculate_Profit/Final/cost_contributors/fmp_cost_cat_perc.csv")

gear_fmp_dist<- read.csv(file="V:/Ardini_Cost_Survey/SAS_Cost_Survey/Profitability_Profiles/Calculate_Profit/Final/cost_contributors/gear_fmp_cost_cat_perc.csv")

# Operating Profit Results


# Total Profit Results


# Discussion


# References
Ardini G., Murphy T., Werner S., Bailey M. 2012. An Overview of the Social Sciences Branch (SSB) Commercial Fishing Business Cost Survey in the Northeast: Protocol and Results for Survey Years 2011, 2012, and 2015. US Dept Commer, Northeast Fish Sci Cent Tech Memo 278. 146 p.

Das C. 2013. An Overview of the Annual Cost Survey Protocol and Results in the Northeast (2007 to 2009). US Dept Commer, Northeast Fish Sci Cent Tech Memo 226. 45 p.

Kitts A., Walden J., Squires D., Travis M., Steiner E., Pfeiffer L., Liese C., Pan M. 2022. NOAA Fisheries Best Practices for Measuring Returns to Fishing Businesses. US Dept Commer, NOAA Tech Memo NMFS-F/SPO-231, 54 p.

(forthcoming) Werner S., Conley E., Ardini G. 2025. Greater Atlantic Region Commercial Fishing Business Cost Survey for 2022: Survey Implementation, Data Processing Methods and Preliminary Results.

