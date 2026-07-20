# <img src="https://images.mindcloud.co/apps/icons/b-cgov-news_1776282290418.png" alt="BC Gov News logo" width="28" height="28"> BC Gov News: Universal API

Read BC government news releases, factsheets, and ministry or topic RSS feeds from the official BC Gov News site.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bCGovNews/latest
- **Category:** Website & App Building / CMS
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://news.gov.bc.ca/
- **Vendor API docs:** https://news.gov.bc.ca/connect

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Agriculture and Food News](actions/list-agriculture-and-food-news.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bCGovNews/latest/actions/list-agriculture-and-food-news?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Announcements

| Action | Method | Description |
| --- | --- | --- |
| [List Agriculture and Food News](actions/list-agriculture-and-food-news.md) | GET | Retrieves Agriculture and Food announcements from BC Gov News. |
| [List Attorney General News](actions/list-attorney-general-news.md) | GET | Retrieves Attorney General announcements from BC Gov News. |
| [List BC Coroners Service News](actions/list-bc-coroners-service-news.md) | GET | Retrieves BC Coroners Service announcements from BC Gov News. |
| [List BC Gov News](actions/list-bc-gov-news.md) | GET | Retrieves the latest announcements from BC Gov News. |
| [List Children and Family Development News](actions/list-children-and-family-development-news.md) | GET | Retrieves Children and Family Development announcements from BC Gov News. |
| [List Citizens Services News](actions/list-citizens-services-news.md) | GET | Retrieves Citizens Services announcements from BC Gov News. |
| [List CleanBC News](actions/list-clean-bc-news.md) | GET | Retrieves CleanBC announcements from BC Gov News. |
| [List Economy News](actions/list-economy-news.md) | GET | Retrieves economy announcements from BC Gov News. |
| [List Education and Child Care News](actions/list-education-and-child-care-news.md) | GET | Retrieves Education and Child Care announcements from BC Gov News. |
| [List Emergency Management and Climate Readiness News](actions/list-emergency-management-and-climate-readiness-news.md) | GET | Retrieves Emergency Management and Climate Readiness announcements from BC Gov News. |
| [List Energy and Climate Solutions News](actions/list-energy-and-climate-solutions-news.md) | GET | Retrieves Energy and Climate Solutions announcements from BC Gov News. |
| [List Environment and Parks News](actions/list-environment-and-parks-news.md) | GET | Retrieves Environment and Parks announcements from BC Gov News. |
| [List Factsheets and Opinion Editorials](actions/list-factsheets-and-opinion-editorials.md) | GET | Retrieves factsheets and opinion editorials from BC Gov News. |
| [List Finance News](actions/list-finance-news.md) | GET | Retrieves finance announcements from BC Gov News. |
| [List Forests News](actions/list-forests-news.md) | GET | Retrieves forests announcements from BC Gov News. |
| [List Government Operations News](actions/list-government-operations-news.md) | GET | Retrieves Government Operations announcements from BC Gov News. |
| [List Health News](actions/list-health-news.md) | GET | Retrieves health announcements from BC Gov News. |
| [List Housing and Municipal Affairs News](actions/list-housing-and-municipal-affairs-news.md) | GET | Retrieves Housing and Municipal Affairs announcements from BC Gov News. |
| [List Indigenous Relations and Reconciliation News](actions/list-indigenous-relations-and-reconciliation-news.md) | GET | Retrieves Indigenous Relations and Reconciliation announcements from BC Gov News. |
| [List Infrastructure News](actions/list-infrastructure-news.md) | GET | Retrieves infrastructure announcements from BC Gov News. |
| [List Intergovernmental Relations Secretariat News](actions/list-intergovernmental-relations-secretariat-news.md) | GET | Retrieves Intergovernmental Relations Secretariat announcements from BC Gov News. |
| [List Jobs and Economic Growth News](actions/list-jobs-and-economic-growth-news.md) | GET | Retrieves Jobs and Economic Growth announcements from BC Gov News. |
| [List Labour News](actions/list-labour-news.md) | GET | Retrieves labour announcements from BC Gov News. |
| [List Mining and Critical Minerals News](actions/list-mining-and-critical-minerals-news.md) | GET | Retrieves Mining and Critical Minerals announcements from BC Gov News. |
| [List Office of the Premier News](actions/list-office-of-the-premier-news.md) | GET | Retrieves Office of the Premier announcements from BC Gov News. |
| [List Post-Secondary Education and Future Skills News](actions/list-post-secondary-education-and-future-skills-news.md) | GET | Retrieves Post-Secondary Education and Future Skills announcements from BC Gov News. |
| [List Public Safety and Solicitor General News](actions/list-public-safety-and-solicitor-general-news.md) | GET | Retrieves Public Safety and Solicitor General announcements from BC Gov News. |
| [List Social Development and Poverty Reduction News](actions/list-social-development-and-poverty-reduction-news.md) | GET | Retrieves Social Development and Poverty Reduction announcements from BC Gov News. |
| [List Tourism Arts Culture and Sport News](actions/list-tourism-arts-culture-and-sport-news.md) | GET | Retrieves Tourism Arts Culture and Sport announcements from BC Gov News. |
| [List Transportation and Transit News](actions/list-transportation-and-transit-news.md) | GET | Retrieves Transportation and Transit announcements from BC Gov News. |

