# <img src="https://images.mindcloud.co/apps/icons/cropped-favikona-01-32x32_1775684762279.png" alt="RECRU logo" width="28" height="28"> RECRU: Universal API

Recruiting software for managing candidates, hiring workflows, and backoffice recruiting operations in RECRU.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rECRU/latest
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.recruhr.com/
- **Vendor API docs:** https://mindclo.recru.eu/api/index/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Echo Text](actions/echo-text.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/echo-text?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Login](actions/login.md) | GET |  |

### Unknown Object

| Action | Method | Description |
| --- | --- | --- |
| [Add Newsletter Unsubscribe](actions/add-newsletter-unsubscribe.md) | POST |  |
| [Echo Text](actions/echo-text.md) | GET |  |
| [Get Allowed Mobile App Menu Items](actions/get-allowed-mobile-app-menu-items.md) | GET |  |
| [Get Client Save Metadata](actions/get-client-save-metadata.md) | GET |  |
| [Get Colors](actions/get-colors.md) | GET |  |
| [Get Country Pairs](actions/get-country-pairs.md) | GET |  |
| [Get Event Types](actions/get-event-types.md) | GET |  |
| [Get Jobseeker Apply Metadata](actions/get-jobseeker-apply-metadata.md) | GET |  |
| [Get Jobseeker Save Metadata](actions/get-jobseeker-save-metadata.md) | GET |  |
| [Get Jobseeker Sources](actions/get-jobseeker-sources.md) | GET |  |
| [Get Locales](actions/get-locales.md) | GET |  |
| [Get Multiple Codebooks](actions/get-multiple-codebooks.md) | GET |  |
| [Get Project Close Reasons](actions/get-project-close-reasons.md) | GET |  |
| [Get Project Save Metadata](actions/get-project-save-metadata.md) | GET |  |
| [Get Rejection Reasons](actions/get-rejection-reasons.md) | GET |  |
| [Get SK NACE Pairs](actions/get-sk-nace-pairs.md) | GET |  |
| [Get User Name Pairs](actions/get-user-name-pairs.md) | GET |  |
| [Ping](actions/ping.md) | GET |  |
| [Remove Newsletter Unsubscribe](actions/remove-newsletter-unsubscribe.md) | DELETE |  |
| [Set Viewed Tour](actions/set-viewed-tour.md) | PUT |  |

