# BC Gov News: Native API Reference

A consolidated summary of BC Gov News's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://news.gov.bc.ca/connect
- **API base URL:** `https://news.gov.bc.ca`

## Authentication

### No Auth

BC Gov News RSS feeds are public and do not require authentication.

This API does not require request authentication.

[Official authentication documentation](https://news.gov.bc.ca/connect)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/rss+xml, application/xml, text/xml;q=0.9` |

Responses from this API use XML. Response data is read from `rss.channel.item`.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Agriculture and Food News](actions/list-agriculture-and-food-news.md) | `GET /ministries/agriculture-and-food/feed` | [docs](https://news.gov.bc.ca/ministries/agriculture-and-food/feed) |
| [List Attorney General News](actions/list-attorney-general-news.md) | `GET /ministries/attorney-general/feed` | [docs](https://news.gov.bc.ca/ministries/attorney-general/feed) |
| [List BC Coroners Service News](actions/list-bc-coroners-service-news.md) | `GET /news-subscribe/bc-coroners-service/feed` | [docs](https://news.gov.bc.ca/news-subscribe/bc-coroners-service/feed) |
| [List BC Gov News](actions/list-bc-gov-news.md) | `GET /feed` | [docs](https://news.gov.bc.ca/feed) |
| [List Children and Family Development News](actions/list-children-and-family-development-news.md) | `GET /ministries/children-and-family-development/feed` | [docs](https://news.gov.bc.ca/ministries/children-and-family-development/feed) |
| [List Citizens Services News](actions/list-citizens-services-news.md) | `GET /ministries/citizens-services/feed` | [docs](https://news.gov.bc.ca/ministries/citizens-services/feed) |
| [List CleanBC News](actions/list-clean-bc-news.md) | `GET /news-subscribe/cleanbc/feed` | [docs](https://news.gov.bc.ca/news-subscribe/cleanbc/feed) |
| [List Economy News](actions/list-economy-news.md) | `GET /sectors/economy/feed` | [docs](https://news.gov.bc.ca/sectors/economy/feed) |
| [List Education and Child Care News](actions/list-education-and-child-care-news.md) | `GET /ministries/education-and-child-care/feed` | [docs](https://news.gov.bc.ca/ministries/education-and-child-care/feed) |
| [List Emergency Management and Climate Readiness News](actions/list-emergency-management-and-climate-readiness-news.md) | `GET /ministries/emergency-management-and-climate-readiness/feed` | [docs](https://news.gov.bc.ca/ministries/emergency-management-and-climate-readiness/feed) |
| [List Energy and Climate Solutions News](actions/list-energy-and-climate-solutions-news.md) | `GET /ministries/energy-and-climate-solutions/feed` | [docs](https://news.gov.bc.ca/ministries/energy-and-climate-solutions/feed) |
| [List Environment and Parks News](actions/list-environment-and-parks-news.md) | `GET /ministries/environment-and-parks/feed` | [docs](https://news.gov.bc.ca/ministries/environment-and-parks/feed) |
| [List Factsheets and Opinion Editorials](actions/list-factsheets-and-opinion-editorials.md) | `GET /factsheets/feed` | [docs](https://news.gov.bc.ca/factsheets/feed) |
| [List Finance News](actions/list-finance-news.md) | `GET /ministries/finance/feed` | [docs](https://news.gov.bc.ca/ministries/finance/feed) |
| [List Forests News](actions/list-forests-news.md) | `GET /ministries/forests/feed` | [docs](https://news.gov.bc.ca/ministries/forests/feed) |
| [List Government Operations News](actions/list-government-operations-news.md) | `GET /sectors/government-operations/feed` | [docs](https://news.gov.bc.ca/sectors/government-operations/feed) |
| [List Health News](actions/list-health-news.md) | `GET /ministries/health/feed` | [docs](https://news.gov.bc.ca/ministries/health/feed) |
| [List Housing and Municipal Affairs News](actions/list-housing-and-municipal-affairs-news.md) | `GET /ministries/housing-and-municipal-affairs/feed` | [docs](https://news.gov.bc.ca/ministries/housing-and-municipal-affairs/feed) |
| [List Indigenous Relations and Reconciliation News](actions/list-indigenous-relations-and-reconciliation-news.md) | `GET /ministries/indigenous-relations-and-reconciliation/feed` | [docs](https://news.gov.bc.ca/ministries/indigenous-relations-and-reconciliation/feed) |
| [List Infrastructure News](actions/list-infrastructure-news.md) | `GET /ministries/infrastructure/feed` | [docs](https://news.gov.bc.ca/ministries/infrastructure/feed) |
| [List Intergovernmental Relations Secretariat News](actions/list-intergovernmental-relations-secretariat-news.md) | `GET /ministries/intergovernmental-relations-secretariat/feed` | [docs](https://news.gov.bc.ca/ministries/intergovernmental-relations-secretariat/feed) |
| [List Jobs and Economic Growth News](actions/list-jobs-and-economic-growth-news.md) | `GET /ministries/jobs-and-economic-growth/feed` | [docs](https://news.gov.bc.ca/ministries/jobs-and-economic-growth/feed) |
| [List Labour News](actions/list-labour-news.md) | `GET /ministries/labour/feed` | [docs](https://news.gov.bc.ca/ministries/labour/feed) |
| [List Mining and Critical Minerals News](actions/list-mining-and-critical-minerals-news.md) | `GET /ministries/mining-and-critical-minerals/feed` | [docs](https://news.gov.bc.ca/ministries/mining-and-critical-minerals/feed) |
| [List Office of the Premier News](actions/list-office-of-the-premier-news.md) | `GET /office-of-the-premier/feed` | [docs](https://news.gov.bc.ca/office-of-the-premier/feed) |
| [List Post-Secondary Education and Future Skills News](actions/list-post-secondary-education-and-future-skills-news.md) | `GET /ministries/post-secondary-education-and-future-skills/feed` | [docs](https://news.gov.bc.ca/ministries/post-secondary-education-and-future-skills/feed) |
| [List Public Safety and Solicitor General News](actions/list-public-safety-and-solicitor-general-news.md) | `GET /ministries/public-safety-and-solicitor-general/feed` | [docs](https://news.gov.bc.ca/ministries/public-safety-and-solicitor-general/feed) |
| [List Social Development and Poverty Reduction News](actions/list-social-development-and-poverty-reduction-news.md) | `GET /ministries/social-development-and-poverty-reduction/feed` | [docs](https://news.gov.bc.ca/ministries/social-development-and-poverty-reduction/feed) |
| [List Tourism Arts Culture and Sport News](actions/list-tourism-arts-culture-and-sport-news.md) | `GET /ministries/tourism-arts-culture-and-sport/feed` | [docs](https://news.gov.bc.ca/ministries/tourism-arts-culture-and-sport/feed) |
| [List Transportation and Transit News](actions/list-transportation-and-transit-news.md) | `GET /ministries/transportation-and-transit/feed` | [docs](https://news.gov.bc.ca/ministries/transportation-and-transit/feed) |
