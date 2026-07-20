# <img src="https://images.mindcloud.co/apps/icons/output-onlinepngtools-1_1776173046219.png" alt="Census Bureau logo" width="28" height="28"> Census Bureau: Universal API

Access U.S. Census Bureau demographic, economic, business, geography, and survey datasets through the Census Data API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/censusBureau/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.census.gov
- **Vendor API docs:** https://www.census.gov/data/developers/guidance/api-user-guide.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Query 2024 ACS 1-Year Detailed Tables](actions/query2024-acs1-detailed-tables.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/censusBureau/latest/actions/query2024-acs1-detailed-tables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Census Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Query 2020 Census Final Self-Response and Return Rates](actions/query2020-census-final-self-response-and-return-rates.md) | GET | Queries Census Bureau 2020 final self-response and return rates. |
| [Query 2020 Census 119th Congressional District](actions/query2020-census119th-congressional-district.md) | GET | Queries Census Bureau 2020 119th congressional district data. |
| [Query 2020 Decennial Demographic and Housing Characteristics](actions/query2020-decennial-demographic-and-housing-characteristics.md) | GET | Queries Census Bureau 2020 decennial demographic and housing characteristics. |
| [Query 2020 Decennial Demographic Profile](actions/query2020-decennial-demographic-profile.md) | GET | Queries Census Bureau 2020 decennial demographic profile data. |
| [Query 2020 Decennial Post-Enumeration Survey](actions/query2020-decennial-post-enumeration-survey.md) | GET | Queries Census Bureau 2020 decennial post-enumeration survey data. |
| [Query 2020 Decennial Redistricting Data](actions/query2020-decennial-redistricting-data.md) | GET | Queries Census Bureau 2020 decennial redistricting data. |
| [Query 2020 Decennial Self-Response Rate](actions/query2020-decennial-self-response-rate.md) | GET | Queries Census Bureau 2020 decennial self-response rate data. |
| [Query 2020 Detailed Demographic and Housing Characteristics File A](actions/query2020-detailed-demographic-and-housing-characteristics-file-a.md) | GET | Queries Census Bureau 2020 detailed demographic and housing characteristics File A. |
| [Query 2020 Detailed Demographic and Housing Characteristics File B](actions/query2020-detailed-demographic-and-housing-characteristics-file-b.md) | GET | Queries Census Bureau 2020 detailed demographic and housing characteristics File B. |
| [Query 2020 Supplemental Demographic and Housing Characteristics](actions/query2020-supplemental-demographic-and-housing-characteristics.md) | GET | Queries Census Bureau 2020 supplemental demographic and housing characteristics. |
| [Query 2021 Population Estimates](actions/query2021-population-estimates.md) | GET | Queries Census Bureau 2021 population estimates. |
| [Query 2022 Economic Census Basic Summary Statistics](actions/query2022-economic-census-basic-summary-statistics.md) | GET | Queries Census Bureau 2022 economic census basic summary statistics. |
| [Query 2022 Economic Census Comparative Statistics](actions/query2022-economic-census-comparative-statistics.md) | GET | Queries Census Bureau 2022 economic census comparative statistics. |
| [Query 2022 Economic Census Establishment and Firm Size](actions/query2022-economic-census-establishment-and-firm-size.md) | GET | Queries Census Bureau 2022 economic census establishment and firm size data. |
| [Query 2022 Economic Census Industry by Product Statistics](actions/query2022-economic-census-industry-by-product-statistics.md) | GET | Queries Census Bureau 2022 economic census industry by product statistics. |
| [Query 2022 Economic Census Products by Industry Statistics](actions/query2022-economic-census-products-by-industry-statistics.md) | GET | Queries Census Bureau 2022 economic census products by industry statistics. |
| [Query 2023 Annual Business Survey Company Summary](actions/query2023-annual-business-survey-company-summary.md) | GET | Queries Census Bureau 2023 annual business survey company summary data. |
| [Query 2023 Annual Business Survey Owners](actions/query2023-annual-business-survey-owners.md) | GET | Queries Census Bureau 2023 annual business survey owners data. |
| [Query 2023 Annual Integrated Economic Survey Nonemployer](actions/query2023-annual-integrated-economic-survey-nonemployer.md) | GET | Queries Census Bureau 2023 annual integrated economic survey nonemployer data. |
| [Query 2023 Community Resilience Estimates](actions/query2023-community-resilience-estimates.md) | GET | Queries Census Bureau 2023 community resilience estimates. |
| [Query 2023 Community Resilience Estimates Puerto Rico](actions/query2023-community-resilience-estimates-puerto-rico.md) | GET | Queries Census Bureau 2023 Puerto Rico community resilience estimates. |
| [Query 2023 County Business Patterns](actions/query2023-county-business-patterns.md) | GET | Queries Census Bureau 2023 county business patterns. |
| [Query 2023 Geography Information](actions/query2023-geography-information.md) | GET | Queries Census Bureau 2023 geography information. |
| [Query 2023 Nonemployer Statistics](actions/query2023-nonemployer-statistics.md) | GET | Queries Census Bureau 2023 nonemployer statistics. |
| [Query 2023 Population Estimates Characteristics](actions/query2023-population-estimates-characteristics.md) | GET | Queries Census Bureau 2023 population estimates characteristics. |
| [Query 2024 ACS 1-Year Comparison Profiles](actions/query2024-acs1-comparison-profiles.md) | GET | Queries Census Bureau 2024 ACS 1-Year comparison profiles. |
| [Query 2024 ACS 1-Year Data Profiles](actions/query2024-acs1-data-profiles.md) | GET | Queries Census Bureau 2024 ACS 1-Year data profiles. |
| [Query 2024 ACS 1-Year Detailed Tables](actions/query2024-acs1-detailed-tables.md) | GET | Queries Census Bureau 2024 ACS 1-Year detailed tables. |
| [Query 2024 ACS 1-Year Selected Population Profiles](actions/query2024-acs1-selected-population-profiles.md) | GET | Queries Census Bureau 2024 ACS 1-Year selected population profiles. |
| [Query 2024 ACS 1-Year Subject Tables](actions/query2024-acs1-subject-tables.md) | GET | Queries Census Bureau 2024 ACS 1-Year subject tables. |
| [Query 2024 ACS 1-Year Supplemental Estimates](actions/query2024-acs1-supplemental-estimates.md) | GET | Queries Census Bureau 2024 ACS 1-Year supplemental estimates. |
| [Query 2024 ACS 5-Year Comparison Profiles](actions/query2024-acs5-comparison-profiles.md) | GET | Queries Census Bureau 2024 ACS 5-Year comparison profiles. |
| [Query 2024 ACS 5-Year Data Profiles](actions/query2024-acs5-data-profiles.md) | GET | Queries Census Bureau 2024 ACS 5-Year data profiles. |
| [Query 2024 ACS 5-Year Detailed Tables](actions/query2024-acs5-detailed-tables.md) | GET | Queries Census Bureau 2024 ACS 5-Year detailed tables. |
| [Query 2024 ACS 5-Year Subject Tables](actions/query2024-acs5-subject-tables.md) | GET | Queries Census Bureau 2024 ACS 5-Year subject tables. |
| [Query 2024 Community Resilience Estimates](actions/query2024-community-resilience-estimates.md) | GET | Queries Census Bureau 2024 community resilience estimates. |
| [Query 2024 Geography Information](actions/query2024-geography-information.md) | GET | Queries Census Bureau 2024 geography information. |
| [Query 2024 Planning Database Block Groups](actions/query2024-planning-database-block-groups.md) | GET | Queries Census Bureau 2024 planning database block groups. |
| [Query 2024 Planning Database Tracts](actions/query2024-planning-database-tracts.md) | GET | Queries Census Bureau 2024 planning database tracts. |
| [Query 2024 Survey of Income and Program Participation](actions/query2024-survey-of-income-and-program-participation.md) | GET | Queries Census Bureau 2024 Survey of Income and Program Participation. |

