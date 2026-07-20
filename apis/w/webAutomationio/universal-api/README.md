# <img src="https://images.mindcloud.co/apps/icons/web-automationio_1775499776245.png" alt="WebAutomation.io logo" width="28" height="28"> WebAutomation.io: Universal API

WebAutomation.io REST API wrapper for extractors, sessions, scraping, and extractor configuration using HTTP Basic auth.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/webAutomationio/latest
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://webautomation.io
- **Vendor API docs:** https://webautomation.io/api/redoc/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Extractors](actions/list-extractors.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/list-extractors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Get Session](actions/get-session.md) | GET | Gets details for a specific extractor session. |
| [List Sessions](actions/list-sessions.md) | GET | Lists all extractor sessions in your account. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Get Session Data](actions/get-session-data.md) | GET | Gets extracted results for a specific session. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Activate Extractor](actions/activate-extractor.md) | PUT | Activates a specific extractor for use. |
| [Add Starter Links](actions/add-starter-links.md) | POST | Replaces an extractor's starter links with a new list. |
| [Delete Starter Links](actions/delete-starter-links.md) | DELETE | Deletes all starter links from a specific extractor. |
| [List Extractor Domains](actions/list-extractor-domains.md) | GET | Lists domains configured for a specific extractor. |
| [List Extractor Variables](actions/list-extractor-variables.md) | GET | Lists variables configured for a specific extractor. |
| [List Extractors](actions/list-extractors.md) | GET | Lists all extractors in your WebAutomation account. |
| [List Extractors by Domain](actions/list-extractors-by-domain.md) | GET | Lists extractors that match a specific domain. |
| [List Starter Links](actions/list-starter-links.md) | GET | Lists starter links configured for a specific extractor. |
| [Update Extractor Variables](actions/update-extractor-variables.md) | PUT | Updates one variable value for a specific extractor. |

