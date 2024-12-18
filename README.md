# The Use of Cost Survey Data to Calculate Vessel Profits for Commercial Fishing Fleets in the Northeast U.S.

# Project Background

Profit is an important metric in assessing the economic performance of commercial fishing fleets and in evaluating the impacts of proposed regulations, as required by applicable laws. Within the Northeast United States, commercial revenues are readily available to NOAA Fisheries, as all federally permitted vessels are required to report sales to licensed dealers. Cost data, on the other hand, have generally been the limiting factor in calculating vessel profits. 
The Northeast Fisheries Science Center conducts a voluntary survey, sent intermittently since the early 2000s, to collect comprehensive cost information from commercial fishing vessel owners. This survey was last implemented during March-July 2023 for costs incurred during calendar year 2022. One of the primary goals of the survey is to calculate vessel-level profits; this goal was communicated throughout the outreach process leading up to and during implementation of the most recent survey. 
Using data primarily collected from the most recent cost survey, this paper highlights the methods/process for calculating 2022 profit for commercial vessels who participated in the survey effort. These methods support the profit snapshots which serve as a key performance metric in evaluating the economic impacts of proposed fishery management actions in the future. 

# NEFSC Social Sciences Branch Cost Survey

Starting in 2007, the Social Sciences Branch (SSB) of the Northeast Fisheries Science Center (NEFSC) has intermittently collected commercial fishing cost information from vessel owners. Information is collected through a voluntary survey which includes questions on costs such as vessel repairs and improvements, vessel insurance, trip expenses, crew payments, and overhead. The most recent survey, formally known as the Greater Atlantic Region Commercial Fishing Business Cost Survey for 2022 (hereafter 2022 cost survey), was fielded in 2023 to collect costs incurred by vessel owners during calendar year 2022. Each owner of a federally permitted commercial fishing vessel that was active in either calendar year 2021 or 2022 received a survey. A total of 2,495 individuals were sent the 2022 cost survey with 422 surveys returned. After accounting for incomplete returned surveys and ineligibles within the sampling frame, the final response rate was 14.8% (367/2,477). This response rate was slightly lower than the 16.8% average response rate over the six previous cost surveys fielded since 2007. For further details on the implementation of the 2022 cost survey see Werner et al. (2024). For more information on early iterations of the cost survey, see Das (2015) and Ardini et al. (2022).

## Survey Respondents

A total of 422 surveys were returned to the Social Sciences Branch at the conclusion of the 2022 cost survey. The profit calculations above were first performed for all 422 observations followed by a series of steps to eliminate those observations that were deemed inappropriate to include in the snapshot.
Filtering of Observations
The first filtering step followed the same process described in Werner et al. 2024 in which returned surveys must have answered at least one cost-related question (Complete_1=1 and REFUSAL_INELIGIBLE_PARTIAL=0). This step eliminated 55 observations, bringing the total  number down to 367. Some surveys were complete but the vessel was inactive during 2022 (vessel activity = “INACTIVE” or “REC_OR_OTHER”); the elimination of these 34 observations brought the total to 333. Additionally, 20 surveys were considered complete and the vessel was active during 2022 but no commercial revenue was found in the CAMS_LAND table. These initial filtering steps left a total of 313 observations. 

Upon completion of the initial filtering steps, a few secondary steps were performed. The survey was divided into sections to evaluate the number of sections skipped for each response. A total of 16 observations out of 313 skipped multiple survey sections. After a brief visual assessment, these observations were deemed to be missing too many potential costs for inclusion. A total of 12 observations out of the remaining 297 skipped one survey section. These cases were more critically evaluated. Four out of the 12 only skipped the crew payment section. Since these were all small vessels with relatively low costs and operating profit, assuming there was no crew onboard was deemed appropriate.

# Profit Calculation Methods

## Metrics
There are a number of different metrics to measure net returns to commercial fishing businesses (Kitts 2022). A cash flow statement, an income statement, and an economic profit statement. A cash flow statement is typically performed over time. An economic profit statement includes the opportunity costs of capital and labor. We choose to provide modified income statements looking at both operating profit and total profit. These two metrics are described below and in Figure 1.
Modified Income Statement: Operating Profit
Operating profit refers to gross revenues minus operating (variable costs). Within the cost survey, two sections in particular cover operating costs. The trip expenses section collects information on fuel, bait, ice, food. The crew payment section includes the total amount to crew and hired captain, as well as any benefits paid out. Outside of the survey, observer costs are also included in the operating profit calculation.
Modified Income Statement: Total Profit
Total profit refers to operating profit minus non-operating costs. These costs can be both fixed and quasi-fixed. Fixed costs include mooring fees, permit fees, and vessel insurance. Within the cost survey, a few different sections 

## Data
### Commercial Revenue
All individuals that were sampled for the 2022 cost survey are owners of federally-permitted commercial fishing vessels active in 2021 or 2022. All federally-permitted vessels are required to sell their catch to federally-licensed seafood dealers. The sales data for 2022 commercial fishing revenue derived from landings occurring in the Northeast region (ME to Cape Hatteras, NC) was accessed through the CAMS_LAND table. This table includes all revenues as recorded in dealer reports, in addition to variables from other data sources, such as Vessel Trip Reports (VTRs) and Permit data. All vessels included in the profit snapshots generated commercial fishing revenue >$0 during 2022.

Primary gear was defined according to the largest contributor to total commercial vessel revenue during 2022. Gear type was derived first from the CAMS_LAND table, using the variable NEGEAR. The gear code was then merged to a dataset of gear groupings constructed as part of the cost survey sampling frame. The dataset groups together NEGEAR codes that are similar into broader categories; for example bottom trawl and midwater trawl both fall into the trawl category. The resulting primary gear groups are as follows: gillnet, handgear, hydraulic dredge, longline, pot/trap, scallop dredge, seine, trawl, and unknown. Due to low response levels for some primary gear groups, results are unable to be presented.

Primary fishery was defined according to the largest contributor to total commercial vessel revenue during 2022. Fishery was first derived from the CAMS_LAND table, using the variable ITIS_GROUP1 to define species. Species were then grouped into Fishery Management Plans (FMPs) according to the table CFG_ITIS. Fisheries include all FMPs under the New England and Mid-Atlantic Fishery Management Councils, as well as American lobster, managed by the Atlantic States Marine Fisheries Commission. All other fisheries are grouped into “Other”. Due to low response levels for some primary fisheries, results are unable to be presented.

### For-Hire Revenue
While the 2022 cost survey was sent to vessels engaged in commercial fishing during 2021 or 2022, some of these vessels also engage in for-hire fishing. In order to most accurately capture vessel-level profits, it is important to include this additional source of revenue when vessels participated in recreational fishing and had commercial revenues greater than $0.00.

Multiple sources were utilized for the estimation of vessel for-hire revenues. First, all 2022 party/charter trips were retrieved from the VESLOG2022T table, in which party/charter trips were defined according to the variable TRIPCATG. Other variables retained from the VESLOG2022T table for these trips include the number of anglers (NANGLERS) and landing state (STATE). Next, average angler charter/guide fees by state were retrieved from the results of the 2022 National Angler Expenditure Survey administered by NOAA Fisheries. State-level averages were used in light of the variability in fees by state within the Northeast region (ME-NC) as well as the high level of response for each state. The average angler fee was then multiplied by the number of anglers for each 2022 party/charter trip by state. Finally, the trip-level revenue and cost calculations were summedcalculated to achieve an annual vessel-level value.calculatedsummed to the vessel-level.

### Survey Costs
The vast majority of cost information used in the calculation of vessel profits came directly from the 2022 cost survey. Some manipulation of the data was required to make it usable at the vessel/annual level. These data manipulation steps are summarized below.

Operating Costs: Survey respondents were given the option of providing operating costs such as fuel, bait, and ice either at the annual level or as an average by trip. For those respondents who filled in the average cost by trip, the value was multiplied by the number of commercial trips during 2022. In general, the number of trips was used directly from the survey (Q2). In cases where this information was not filled in, the number of trips was retrieved from the CAMS_LAND table in which a unique combination of VTR DOCID and Landing Date represented a vessel trip.

Overhead Costs: Survey respondents were given the option of providing these costs either at the vessel level or at the business level. For those respondents who filled in business level costs, the value was divided by the number of vessels owned by the respondent during 2022. The number of vessels owned was taken directly from the survey (Q13).

Quota Leasing Costs: Survey respondents were given the option to provide quota leasing costs either at the vessel-level or across multiple vessels. If this cost was provided across multiple vessels, the value was divided by the specific number of vessels the quota leasing cost was attributed to (Q17).

Other Costs: At the end of the survey, respondents were given the opportunity to list other costs that were not included in the survey. When other costs were listed, they were evaluated on a case-by-case basis (see Werner et al. 2024). Those that could not be allocated to an existing cost category were excluded from the profit calculation.


### Other Costs
#### Observer Costs
As covered in the previous section, the 2022 cost survey queried a variety of expenses faced by vessel owners. During pre-testing of the survey instrument, fishing industry members generally felt that the survey did a good job of including all significant costs. Furthermore, comments on the survey itself and a lack of other costs filled in by respondents indicated the survey covered significant costs. However there are two costs, crew supplies and freshwater, that are collected by at-sea observers that were not included in the 2022 cost survey. 

To capture these costs, data from the observer programs was used to calculate average costs per trip by gear. First, all 2022 trips from the tables OBTRP and ASMTRP were retrieved, with the relevant cost variables SUPPLYCOST and WATERCOST. Next, primary gear by trip was defined by using the CAMS_LAND table, and the same process highlighted in the Commercial Revenue section. An intermediate table (MATCH_OBS) was then used to merge the CAMS data with the observer data. Once merged, the average crew supply and freshwater trip costs by gear type were calculated. These averages were merged by gear with all of the trips taken by survey responding vessels during 2022. Finally, trip-level costs were summed to the vessel-level.

#### Depreciation
The final cost component included in the profit calculation is vessel depreciation. Ideally, a different depreciation value would be assigned to each capital component (e.g. electronics, engine, hull) using the age of the equipment. This method would require additional information beyond that collected in the 2022 cost survey.

The cost survey does ask for information on Vessel Value. However, responses to this question was lower than most other survey questions. Part of the lower number of values provided for this question is the option for “I Prefer not to Answer” was  included. This option was not included for any other survey questions. In light of the lower response rate, an alternate method was used to estimate vessel value. The method used the responses from the 2022 survey and previous cost surveys to estimate shadow values of vessel characteristics such as age, length, and type of construction. The first step in performing this estimation involved merging in vessel characteristics from the PERMIT_VPS_VESSEL table. A depreciation cost was applied to the vessel value at different rates depending on the age of the vessel. 

# Results

## By Primary Gear

## By Primary Gear/FMP

# Future work 

# References
Ardini G., Murphy T., Werner S., Bailey M. 2012. An Overview of the Social Sciences Branch (SSB) Commercial Fishing Business Cost Survey in the Northeast: Protocol and Results for Survey Years 2011, 2012, and 2015. US Dept Commer, Northeast Fish Sci Cent Tech Memo 278. 146 p.

Das C. 2013. An Overview of the Annual Cost Survey Protocol and Results in the Northeast (2007 to 2009). US Dept Commer, Northeast Fish Sci Cent Tech Memo 226. 45 p.

Kitts A., Walden J., Squires D., Travis M., Steiner E., Pfeiffer L., Liese C., Pan M. 2022. NOAA Fisheries Best Practices for Measuring Returns to Fishing Businesses. US Dept Commer, NOAA Tech Memo NMFS-F/SPO-231, 54 p.


