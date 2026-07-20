# Census Bureau: Native API Reference

A consolidated summary of Census Bureau's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.census.gov/data/developers/guidance/api-user-guide.html
- **API base URL:** `https://api.census.gov/data`

## Authentication

### API Key

Use a Census Data API key as the shared query parameter `key` on Census API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.census.gov/data/developers/guidance/api-user-guide.html)

## API conventions

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `get` | query | `string` | yes | Comma-separated Census variables to return, such as NAME,B01001_001E. Send multiple values as a string separated by `,`. |
| `for` | query | `string` | no | Census geography predicate, such as state:* or us:1. |
| `in` | query | `string` | no | Parent geography predicate for smaller geographies, such as state:01 county:001. |
| `ucgid` | query | `string` | no | Optional Census uniform geographic identifier predicate. |
| `descriptive` | query | `boolean` | no | When true, Census includes variable labels in the API output. |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Query 2020 Census Final Self-Response and Return Rates](actions/query2020-census-final-self-response-and-return-rates.md) | `GET /2020/dec/selfresponserate` | [docs](https://api.census.gov/data/2020/dec/selfresponserate.html) |
| [Query 2020 Census 119th Congressional District](actions/query2020-census119th-congressional-district.md) | `GET /2020/dec/cd119` | [docs](https://api.census.gov/data/2020/dec/cd119.html) |
| [Query 2020 Decennial Demographic and Housing Characteristics](actions/query2020-decennial-demographic-and-housing-characteristics.md) | `GET /2020/dec/dhc` | [docs](https://api.census.gov/data/2020/dec/dhc.html) |
| [Query 2020 Decennial Demographic Profile](actions/query2020-decennial-demographic-profile.md) | `GET /2020/dec/dp` | [docs](https://api.census.gov/data/2020/dec/dp.html) |
| [Query 2020 Decennial Post-Enumeration Survey](actions/query2020-decennial-post-enumeration-survey.md) | `GET /2020/dec/pes` | [docs](https://api.census.gov/data/2020/dec/pes.html) |
| [Query 2020 Decennial Redistricting Data](actions/query2020-decennial-redistricting-data.md) | `GET /2020/dec/pl` | [docs](https://api.census.gov/data/2020/dec/pl.html) |
| [Query 2020 Decennial Self-Response Rate](actions/query2020-decennial-self-response-rate.md) | `GET /2020/dec/responserate` | [docs](https://api.census.gov/data/2020/dec/responserate.html) |
| [Query 2020 Detailed Demographic and Housing Characteristics File A](actions/query2020-detailed-demographic-and-housing-characteristics-file-a.md) | `GET /2020/dec/ddhca` | [docs](https://api.census.gov/data/2020/dec/ddhca.html) |
| [Query 2020 Detailed Demographic and Housing Characteristics File B](actions/query2020-detailed-demographic-and-housing-characteristics-file-b.md) | `GET /2020/dec/ddhcb` | [docs](https://api.census.gov/data/2020/dec/ddhcb.html) |
| [Query 2020 Supplemental Demographic and Housing Characteristics](actions/query2020-supplemental-demographic-and-housing-characteristics.md) | `GET /2020/dec/sdhc` | [docs](https://api.census.gov/data/2020/dec/sdhc.html) |
| [Query 2021 Population Estimates](actions/query2021-population-estimates.md) | `GET /2021/pep/population` | [docs](https://api.census.gov/data/2021/pep/population.html) |
| [Query 2022 Economic Census Basic Summary Statistics](actions/query2022-economic-census-basic-summary-statistics.md) | `GET /2022/ecnbasic` | [docs](https://api.census.gov/data/2022/ecnbasic.html) |
| [Query 2022 Economic Census Comparative Statistics](actions/query2022-economic-census-comparative-statistics.md) | `GET /2022/ecncomp` | [docs](https://api.census.gov/data/2022/ecncomp.html) |
| [Query 2022 Economic Census Establishment and Firm Size](actions/query2022-economic-census-establishment-and-firm-size.md) | `GET /2022/ecnsize` | [docs](https://api.census.gov/data/2022/ecnsize.html) |
| [Query 2022 Economic Census Industry by Product Statistics](actions/query2022-economic-census-industry-by-product-statistics.md) | `GET /2022/ecnnapcsind` | [docs](https://api.census.gov/data/2022/ecnnapcsind.html) |
| [Query 2022 Economic Census Products by Industry Statistics](actions/query2022-economic-census-products-by-industry-statistics.md) | `GET /2022/ecnnapcsprd` | [docs](https://api.census.gov/data/2022/ecnnapcsprd.html) |
| [Query 2023 Annual Business Survey Company Summary](actions/query2023-annual-business-survey-company-summary.md) | `GET /2023/abscs` | [docs](https://api.census.gov/data/2023/abscs.html) |
| [Query 2023 Annual Business Survey Owners](actions/query2023-annual-business-survey-owners.md) | `GET /2023/abscbo` | [docs](https://api.census.gov/data/2023/abscbo.html) |
| [Query 2023 Annual Integrated Economic Survey Nonemployer](actions/query2023-annual-integrated-economic-survey-nonemployer.md) | `GET /2023/aiesnonemp` | [docs](https://api.census.gov/data/2023/aiesnonemp.html) |
| [Query 2023 Community Resilience Estimates](actions/query2023-community-resilience-estimates.md) | `GET /2023/cre` | [docs](https://api.census.gov/data/2023/cre.html) |
| [Query 2023 Community Resilience Estimates Puerto Rico](actions/query2023-community-resilience-estimates-puerto-rico.md) | `GET /2023/crepuertorico` | [docs](https://api.census.gov/data/2023/crepuertorico.html) |
| [Query 2023 County Business Patterns](actions/query2023-county-business-patterns.md) | `GET /2023/cbp` | [docs](https://api.census.gov/data/2023/cbp.html) |
| [Query 2023 Geography Information](actions/query2023-geography-information.md) | `GET /2023/geoinfo` | [docs](https://api.census.gov/data/2023/geoinfo.html) |
| [Query 2023 Nonemployer Statistics](actions/query2023-nonemployer-statistics.md) | `GET /2023/nonemp` | [docs](https://api.census.gov/data/2023/nonemp.html) |
| [Query 2023 Population Estimates Characteristics](actions/query2023-population-estimates-characteristics.md) | `GET /2023/pep/charv` | [docs](https://api.census.gov/data/2023/pep/charv.html) |
| [Query 2024 ACS 1-Year Comparison Profiles](actions/query2024-acs1-comparison-profiles.md) | `GET /2024/acs/acs1/cprofile` | [docs](https://api.census.gov/data/2024/acs/acs1/cprofile.html) |
| [Query 2024 ACS 1-Year Data Profiles](actions/query2024-acs1-data-profiles.md) | `GET /2024/acs/acs1/profile` | [docs](https://api.census.gov/data/2024/acs/acs1/profile.html) |
| [Query 2024 ACS 1-Year Detailed Tables](actions/query2024-acs1-detailed-tables.md) | `GET /2024/acs/acs1` | [docs](https://api.census.gov/data/2024/acs/acs1.html) |
| [Query 2024 ACS 1-Year Selected Population Profiles](actions/query2024-acs1-selected-population-profiles.md) | `GET /2024/acs/acs1/spp` | [docs](https://api.census.gov/data/2024/acs/acs1/spp.html) |
| [Query 2024 ACS 1-Year Subject Tables](actions/query2024-acs1-subject-tables.md) | `GET /2024/acs/acs1/subject` | [docs](https://api.census.gov/data/2024/acs/acs1/subject.html) |
| [Query 2024 ACS 1-Year Supplemental Estimates](actions/query2024-acs1-supplemental-estimates.md) | `GET /2024/acs/acsse` | [docs](https://api.census.gov/data/2024/acs/acsse.html) |
| [Query 2024 ACS 5-Year Comparison Profiles](actions/query2024-acs5-comparison-profiles.md) | `GET /2024/acs/acs5/cprofile` | [docs](https://api.census.gov/data/2024/acs/acs5/cprofile.html) |
| [Query 2024 ACS 5-Year Data Profiles](actions/query2024-acs5-data-profiles.md) | `GET /2024/acs/acs5/profile` | [docs](https://api.census.gov/data/2024/acs/acs5/profile.html) |
| [Query 2024 ACS 5-Year Detailed Tables](actions/query2024-acs5-detailed-tables.md) | `GET /2024/acs/acs5` | [docs](https://api.census.gov/data/2024/acs/acs5.html) |
| [Query 2024 ACS 5-Year Subject Tables](actions/query2024-acs5-subject-tables.md) | `GET /2024/acs/acs5/subject` | [docs](https://api.census.gov/data/2024/acs/acs5/subject.html) |
| [Query 2024 Community Resilience Estimates](actions/query2024-community-resilience-estimates.md) | `GET /2024/cre` | [docs](https://api.census.gov/data/2024/cre.html) |
| [Query 2024 Geography Information](actions/query2024-geography-information.md) | `GET /2024/geoinfo` | [docs](https://api.census.gov/data/2024/geoinfo.html) |
| [Query 2024 Planning Database Block Groups](actions/query2024-planning-database-block-groups.md) | `GET /2024/pdb/blockgroup` | [docs](https://api.census.gov/data/2024/pdb/blockgroup.html) |
| [Query 2024 Planning Database Tracts](actions/query2024-planning-database-tracts.md) | `GET /2024/pdb/tract` | [docs](https://api.census.gov/data/2024/pdb/tract.html) |
| [Query 2024 Survey of Income and Program Participation](actions/query2024-survey-of-income-and-program-participation.md) | `GET /2024/sipp` | [docs](https://api.census.gov/data/2024/sipp.html) |
