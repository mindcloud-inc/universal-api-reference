# <img src="https://images.mindcloud.co/apps/icons/metance_1776966611702.png" alt="Metance logo" width="28" height="28"> Metance: Universal API

Connect Metance to read workspace dashboards, sessions, content, topics, folders, content sets, company data, and files from your corporate memory workspace.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/metance/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.metance.com
- **Vendor API docs:** https://api.metance.com/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Company](actions/get-current-company.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-current-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Content Types](actions/get-content-types.md) | GET | Retrieves content types from the current Metance workspace. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Company](actions/get-current-company.md) | GET | Retrieves the current company from Metance. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [List Files](actions/list-files.md) | GET | Retrieves files from the current Metance workspace. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Get Folders](actions/get-folders.md) | GET | Retrieves folders from the current Metance workspace. |

### Knowledge Articles

| Action | Method | Description |
| --- | --- | --- |
| [Get Content By ID](actions/get-content-by-id.md) | GET | Retrieves content from Metance by ID. |
| [Get Content By URL](actions/get-content-by-url.md) | GET | Retrieves content from Metance by URL. |
| [Get Section Contents](actions/get-section-contents.md) | GET | Retrieves contents from a specific Metance section. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Get Topics](actions/get-topics.md) | GET | Retrieves topics from the current Metance workspace. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Session](actions/get-current-session.md) | GET | Retrieves the current session from Metance. |

