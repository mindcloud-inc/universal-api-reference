# Zoominfo: Native API Reference

A consolidated summary of Zoominfo's API configuration and 84 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.zoominfo.com/
- **API base URL:** `https://api.zoominfo.com/`

## Authentication

### Custom

### Credentials

- **User Name:** `userName` · required
- **Password:** `password` · required

Send these headers with each API request:

```http
Authorization: Bearer <custom.jwt>
```

[Official authentication documentation](https://api-docs.zoominfo.com/#477888fc-8308-4645-81ca-ca7a6d7ba3d1)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Response data is read from `data`. The total page count is read from `totalResults`. The current page number is read from `currentPage`.

## Pagination

Use `rpp` in the request body to set the page size (default 25; accepted range 1–100). Use `page` in the request body to choose the page; numbering starts at 1.

## Endpoints (84 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | `POST authenticate` | [docs](https://api-docs.zoominfo.com/#477888fc-8308-4645-81ca-ca7a6d7ba3d1) |
| [Enrich Company](actions/enrich-company.md) | `POST enrich/company` | [docs](https://api-docs.zoominfo.com/#59a59d9e-7eb9-44fa-904a-f10f9ab7c5fd) |
| [Enrich Company Master Data](actions/enrich-company-master-data.md) | `POST enrich/company-master` | [docs](https://api-docs.zoominfo.com/#8b6cffe4-cb34-44ab-ad5d-1953d372ffd3) |
| [Enrich Contact](actions/enrich-contact.md) | `POST enrich/contact` | [docs](https://api-docs.zoominfo.com/#c145dd01-eb54-4fc2-bbdb-9edc04b7ea1b) |
| [Enrich Corporate Hierarchy](actions/enrich-corporate-hierarchy.md) | `POST enrich/corporatehierarchy` | [docs](https://api-docs.zoominfo.com/#1bf83184-9ee9-478f-b839-9afab4dfe18e) |
| [Enrich Hashtags](actions/enrich-hashtags.md) | `POST enrich/hashtag` | [docs](https://api-docs.zoominfo.com/#886fb5cc-b587-4f26-bd68-892798d45ffe) |
| [Enrich Intent](actions/enrich-intent.md) | `POST enrich/intent` | [docs](https://api-docs.zoominfo.com/#48c36a9f-e4eb-4ce8-8080-a7b810df7c2d) |
| [Enrich Location](actions/enrich-location.md) | `POST enrich/location` | [docs](https://api-docs.zoominfo.com/#2b221ad0-f6c2-40cb-b721-6513e90afd8d) |
| [Enrich News](actions/enrich-news.md) | `POST enrich/news` | [docs](https://api-docs.zoominfo.com/#a04f60d9-353e-4eb1-9c37-0539ee6b8d13) |
| [Enrich Org Chart](actions/enrich-org-chart.md) | `POST enrich/orgchart` | [docs](https://api-docs.zoominfo.com/#763b3c10-41d1-4d52-9775-1712f712202e) |
| [Enrich Scoops](actions/enrich-scoops.md) | `POST enrich/scoop` | [docs](https://api-docs.zoominfo.com/#545c603a-fbe5-48b6-b4b4-bdca626fead0) |
| [Enrich Technology](actions/enrich-technology.md) | `POST enrich/tech` | [docs](https://api-docs.zoominfo.com/#9fc40c02-fe95-448f-a6f4-e903c85c81a9) |
| [Get Board Members](actions/get-board-members.md) | `GET lookup/boardMember` | [docs](https://api-docs.zoominfo.com/#993c5474-f201-4de8-9e64-f87c2045a084) |
| [Get Buying Groups](actions/get-buying-groups.md) | `GET lookup/buyinggroups` | [docs](https://api-docs.zoominfo.com/#595ddead-d5b6-461f-ae4a-d3952c7776f6) |
| [Get Company Enrich Inputs](actions/get-company-enrich-inputs.md) | `GET lookup/inputfields/company/enrich` | [docs](https://api-docs.zoominfo.com/#7a915792-e8cd-4e3a-9f0e-c19b850be536) |
| [Get Company Enrich Outputs](actions/get-company-enrich-outputs.md) | `GET lookup/outputfields/company/enrich` | [docs](https://api-docs.zoominfo.com/#d05239c3-2597-45f8-9384-f2dbd3518cfc) |
| [Get Company Master Data Enrich Inputs](actions/get-company-master-data-enrich-inputs.md) | `GET lookup/inputfields/company-master/enrich` | [docs](https://api-docs.zoominfo.com/#d305402c-33d1-488c-8b8f-b5b079868a61) |
| [Get Company Master Data Enrich Outputs](actions/get-company-master-data-enrich-outputs.md) | `GET lookup/outputfields/company-master/enrich` | [docs](https://api-docs.zoominfo.com/#58b47522-753a-4104-a0c6-454adf4b6a1d) |
| [Get Company Ranking](actions/get-company-ranking.md) | `GET lookup/companyranking` | [docs](https://api-docs.zoominfo.com/#217297b2-9743-47b5-a2be-adf5be3bdd47) |
| [Get Company Search Inputs](actions/get-company-search-inputs.md) | `GET lookup/inputfields/company/search` | [docs](https://api-docs.zoominfo.com/#ffd4ccc6-09d1-4026-8c4f-863d02fd703e) |
| [Get Company Search Outputs](actions/get-company-search-outputs.md) | `GET lookup/outputfields/company/search` | [docs](https://api-docs.zoominfo.com/#3dd35354-8523-4a8c-935a-97ed56d059a6) |
| [Get Company Type](actions/get-company-type.md) | `GET lookup/companytype` | [docs](https://api-docs.zoominfo.com/#c1c18376-e740-4412-9d86-dbd1145429c8) |
| [Get Compliance Inputs](actions/get-compliance-inputs.md) | `GET lookup/inputfields/compliance/enrich` | [docs](https://api-docs.zoominfo.com/#b45d0781-0844-4c51-bb2e-f2656e1af919) |
| [Get Compliance Outputs](actions/get-compliance-outputs.md) | `GET lookup/outputfields/compliance/enrich` | [docs](https://api-docs.zoominfo.com/#0c06b63c-9d07-40e3-a4ea-6f2e3fd10222) |
| [Get Contact Departments](actions/get-contact-departments.md) | `GET lookup/department` | [docs](https://api-docs.zoominfo.com/#015c9e39-dc39-41dc-ab33-5f07a802fd99) |
| [Get Contact Enrich Inputs](actions/get-contact-enrich-inputs.md) | `GET lookup/inputfields/contact/enrich` | [docs](https://api-docs.zoominfo.com/#dbaf31cd-0f7a-4bf3-b6c1-077f3c31f2df) |
| [Get Contact Enrich Outputs](actions/get-contact-enrich-outputs.md) | `GET lookup/outputfields/contact/enrich` | [docs](https://api-docs.zoominfo.com/#28b47784-3186-4fc4-af91-12e6bc6fb31a) |
| [Get Contact Search Inputs](actions/get-contact-search-inputs.md) | `GET lookup/inputfields/contact/search` | [docs](https://api-docs.zoominfo.com/#74630827-dd25-4b6a-bf72-f7cfeffd6c41) |
| [Get Contact Search Outputs](actions/get-contact-search-outputs.md) | `GET lookup/outputfields/contact/search` | [docs](https://api-docs.zoominfo.com/#5ed629a9-f24a-41a3-bc66-89f3f09f051c) |
| [Get Continents](actions/get-continents.md) | `GET lookup/continent` | [docs](https://api-docs.zoominfo.com/#6bd81cb6-26d6-4d43-911e-df5844830bd9) |
| [Get Corporate Hierarchy Enrich Inputs](actions/get-corporate-hierarchy-enrich-inputs.md) | `GET lookup/inputfields/corporatehierarchy/enrich` | [docs](https://api-docs.zoominfo.com/#d72da288-2069-47c9-b36f-16cdab5d9988) |
| [Get Corporate Hierarchy Enrich Outputs](actions/get-corporate-hierarchy-enrich-outputs.md) | `GET lookup/outputfields/corporatehierarchy/enrich` | [docs](https://api-docs.zoominfo.com/#d6813026-dcae-4b20-9ee4-b1301451a2c7) |
| [Get Countries](actions/get-countries.md) | `GET lookup/country` | [docs](https://api-docs.zoominfo.com/#ea0670fa-381d-4e1f-a087-8b4b179b691b) |
| [Get Employee Category Band](actions/get-employee-category-band.md) | `GET lookup/employee-category-band` | [docs](https://api-docs.zoominfo.com/#1949fef9-edee-4079-a6de-5acff2b07f44) |
| [Get Employee Count](actions/get-employee-count.md) | `GET lookup/employeecount` | [docs](https://api-docs.zoominfo.com/#4632ac8d-d96b-4672-ba84-8314ba1bb146) |
| [Get Hashtag](actions/get-hashtag.md) | `GET lookup/hashtag` | [docs](https://api-docs.zoominfo.com/#fca6515f-0ef5-4f6a-885d-9c80aef81f14) |
| [Get Hashtag Enrich Inputs](actions/get-hashtag-enrich-inputs.md) | `GET lookup/inputfields/hashtag/enrich` | [docs](https://api-docs.zoominfo.com/#a7bea20a-f496-431b-9403-337231c4a22e) |
| [Get Hierarchy Code](actions/get-hierarchy-code.md) | `GET lookup/hierarchy-code` | [docs](https://api-docs.zoominfo.com/#43513c41-3f30-4419-9b47-472b46bb5f9c) |
| [Get Industry Codes](actions/get-industry-codes.md) | `GET lookup/industry` | [docs](https://api-docs.zoominfo.com/#e1f93c82-43bc-4bdc-9600-03242ef873ca) |
| [Get Intent Enrich Inputs](actions/get-intent-enrich-inputs.md) | `GET lookup/inputfields/intent/enrich` | [docs](https://api-docs.zoominfo.com/#2dcbe844-7f1f-45f3-ae32-2598ccec5be4) |
| [Get Intent Enrich Outputs](actions/get-intent-enrich-outputs.md) | `GET lookup/outputfields/intent/enrich` | [docs](https://api-docs.zoominfo.com/#fc4083cf-6179-4f0f-8b9b-80aedc2e3e67) |
| [Get Intent Search Inputs](actions/get-intent-search-inputs.md) | `GET lookup/inputfields/intent/search` | [docs](https://api-docs.zoominfo.com/#14669274-88b8-4762-8d61-57d2fd5abf12) |
| [Get Intent Search Outputs](actions/get-intent-search-outputs.md) | `GET lookup/outputfields/intent/search` | [docs](https://api-docs.zoominfo.com/#8f3540ee-4093-48e4-aebb-97133a864912) |
| [Get IP Enrich Inputs](actions/get-ip-enrich-inputs.md) | `GET lookup/inputfields/ip/enrich` | [docs](https://api-docs.zoominfo.com/#12a5c22b-cba1-4b40-a8c6-45f564cf0c2a) |
| [Get IP Enrich Outputs](actions/get-ip-enrich-outputs.md) | `GET lookup/outputfields/ip/enrich` | [docs](https://api-docs.zoominfo.com/#ca8c2c2f-c731-4310-ae0d-dfba2fb756d7) |
| [Get Job Function](actions/get-job-function.md) | `GET lookup/jobfunction` | [docs](https://api-docs.zoominfo.com/#dd9e9fa4-33aa-495a-ab40-f97339784cf1) |
| [Get Job Title Hierarchy](actions/get-job-title-hierarchy.md) | `GET lookup/jobtitlehierarchy` | [docs](https://api-docs.zoominfo.com/#abe7fe05-05e7-414a-95a5-46fc5cc70512) |
| [Get Location Enrich Inputs](actions/get-location-enrich-inputs.md) | `GET lookup/inputfields/location/enrich` | [docs](https://api-docs.zoominfo.com/#5517cdb0-18c9-40ad-9d80-bdee7872d9e0) |
| [Get Location Enrich Outputs](actions/get-location-enrich-outputs.md) | `GET lookup/outputfields/location/enrich` | [docs](https://api-docs.zoominfo.com/#d1fbccf4-2224-4ba8-b72c-5b15e250c2f7) |
| [Get Management Levels](actions/get-management-levels.md) | `GET lookup/managementLevel` | [docs](https://api-docs.zoominfo.com/#239048f1-a720-46b1-a907-3a9ca243ede2) |
| [Get Metro Area](actions/get-metro-area.md) | `GET lookup/metroarea` | [docs](https://api-docs.zoominfo.com/#5fecca5e-74f1-4d39-b6a6-1e0ddf0fa539) |
| [Get NAICS Codes](actions/get-naics-codes.md) | `GET lookup/naicscode` | [docs](https://api-docs.zoominfo.com/#7976cc65-e360-49e7-825a-30d57ae5c091) |
| [Get News Categories](actions/get-news-categories.md) | `GET lookup/news/categories` | [docs](https://api-docs.zoominfo.com/#b9f5ee4a-3287-414c-b244-ddd6f3c0e3fe) |
| [Get News Enrich Inputs](actions/get-news-enrich-inputs.md) | `GET lookup/inputfields/news/enrich` | [docs](https://api-docs.zoominfo.com/#d58425e5-a4a4-4af0-ad01-fa7bbf91ca84) |
| [Get News Enrich Outputs](actions/get-news-enrich-outputs.md) | `GET lookup/outputfields/news/enrich` | [docs](https://api-docs.zoominfo.com/#254b86e3-e51b-450d-8704-95e4da168874) |
| [Get News Search Inputs](actions/get-news-search-inputs.md) | `GET lookup/inputfields/news/search` | [docs](https://api-docs.zoominfo.com/#90bfb6fb-2754-478b-b42d-f8c507ffffb2) |
| [Get News Search Outputs](actions/get-news-search-outputs.md) | `GET lookup/outputfields/news/search` | [docs](https://api-docs.zoominfo.com/#354f6240-e3d3-4c8c-9684-86569fd71581) |
| [Get Org Chart Enrich Inputs](actions/get-org-chart-enrich-inputs.md) | `GET lookup/inputfields/orgchart/enrich` | [docs](https://api-docs.zoominfo.com/#751a9156-1867-4033-a115-a44aa0ecbfad) |
| [Get Org Chart Enrich Outputs](actions/get-org-chart-enrich-outputs.md) | `GET lookup/outputfields/orgchart/enrich` | [docs](https://api-docs.zoominfo.com/#b2c219d2-df68-4ccd-9914-c7c58218f768) |
| [Get Revenue Category Band](actions/get-revenue-category-band.md) | `GET lookup/revenue-category-band` | [docs](https://api-docs.zoominfo.com/#370c8c31-d225-463c-bc05-3af2e904ae40) |
| [Get Revenue Range](actions/get-revenue-range.md) | `GET lookup/revenuerange` | [docs](https://api-docs.zoominfo.com/#77fedfbc-c8df-4e4e-afc2-37112caa97be) |
| [Get Scoop Departments](actions/get-scoop-departments.md) | `GET lookup/scoopdepartment` | [docs](https://api-docs.zoominfo.com/#1649ad68-8e03-4d1f-90ff-ec221d53caa0) |
| [Get Scoop Enrich Inputs](actions/get-scoop-enrich-inputs.md) | `GET lookup/inputfields/scoop/enrich` | [docs](https://api-docs.zoominfo.com/#4ebf5d05-d819-4336-977f-2fe72dc6ac19) |
| [Get Scoop Enrich Outputs](actions/get-scoop-enrich-outputs.md) | `GET lookup/outputfields/scoop/enrich` | [docs](https://api-docs.zoominfo.com/#3af4b7ad-e694-4202-81c4-20b7bab73946) |
| [Get Scoop Search Inputs](actions/get-scoop-search-inputs.md) | `GET lookup/inputfields/scoop/search` | [docs](https://api-docs.zoominfo.com/#1888a5e1-6a96-4cc2-910b-70e574370996) |
| [Get Scoop Search Outputs](actions/get-scoop-search-outputs.md) | `GET lookup/outputfields/scoop/search` | [docs](https://api-docs.zoominfo.com/#185aa18e-02fa-440e-a691-b8e2c391a456) |
| [Get Scoop Topics](actions/get-scoop-topics.md) | `GET lookup/scooptopic` | [docs](https://api-docs.zoominfo.com/#c9aadb87-22ca-4feb-94cc-a73e4540ac94) |
| [Get Scoop Types](actions/get-scoop-types.md) | `GET lookup/scooptype` | [docs](https://api-docs.zoominfo.com/#21aa31de-253e-494f-9408-db442ff9bbb6) |
| [Get SIC Codes](actions/get-sic-codes.md) | `GET lookup/siccode` | [docs](https://api-docs.zoominfo.com/#e72b89cd-7227-4e75-a31c-9dac98458b96) |
| [Get States](actions/get-states.md) | `GET lookup/state` | [docs](https://api-docs.zoominfo.com/#aa538d1b-7c1c-465a-8a03-d7d98314e74d) |
| [Get Sub Unit Type](actions/get-sub-unit-type.md) | `GET lookup/subunittypes` | [docs](https://api-docs.zoominfo.com/#e7dd47c9-bfa4-4dfd-8547-3334377fef17) |
| [Get Tech Categories](actions/get-tech-categories.md) | `GET lookup/tech/category` | [docs](https://api-docs.zoominfo.com/#b73c7096-268f-4bcd-b6a9-cb764f40a29e) |
| [Get Tech Product](actions/get-tech-product.md) | `GET lookup/tech/product` | [docs](https://api-docs.zoominfo.com/#9551cace-281d-43d0-8685-dd39c82780cc) |
| [Get Tech Skills](actions/get-tech-skills.md) | `GET lookup/tech-skills` | [docs](https://api-docs.zoominfo.com/#413af8b8-bfea-47e4-8809-fe1973155067) |
| [Get Tech Vendor](actions/get-tech-vendor.md) | `GET lookup/tech/vendor` | [docs](https://api-docs.zoominfo.com/#b6c19398-eeb4-46c8-a78b-ed51f16e4d0d) |
| [Get Technology Enrich Inputs](actions/get-technology-enrich-inputs.md) | `GET lookup/inputfields/tech/enrich` | [docs](https://api-docs.zoominfo.com/#2cc6abbc-e782-4ab4-80e8-ce29ed17ee4e) |
| [Get Usage](actions/get-usage.md) | `GET lookup/usage` | [docs](https://api-docs.zoominfo.com/#83f8fa61-a04c-4b61-9489-aacd35cfa8c3) |
| [Get Years Of Experience](actions/get-years-of-experience.md) | `GET lookup/years-of-experience` | [docs](https://api-docs.zoominfo.com/#b9407739-7b4a-4283-8c4d-94d7ceb7cbbd) |
| [List Companies](actions/list-companies.md) | `POST search/company` | [docs](https://api-docs.zoominfo.com/#4506f0ad-9147-4016-991f-ce8ef6700f07) |
| [List Contacts](actions/list-contacts.md) | `POST search/contact` | [docs](https://api-docs.zoominfo.com/#2e5121fd-df42-41a4-95d6-0e8f24eebd92) |
| [List Intent](actions/list-intent.md) | `POST search/intent` | [docs](https://api-docs.zoominfo.com/#93f940a4-4381-49dd-8fbc-42cbc75a7a39) |
| [List News](actions/list-news.md) | `POST search/news` | [docs](https://api-docs.zoominfo.com/#4c4c979b-4495-4a17-8925-7d00c52c7e19) |
| [List Scoops](actions/list-scoops.md) | `POST search/scoop` | [docs](https://api-docs.zoominfo.com/#3099d72f-6857-4432-89c2-736410680e60) |
| [Lookup Intent Topics](actions/lookup-intent-topics.md) | `GET lookup/intent/topics` | [docs](https://api-docs.zoominfo.com/#7d3e2352-9099-4207-815e-6129c95a2f16) |
