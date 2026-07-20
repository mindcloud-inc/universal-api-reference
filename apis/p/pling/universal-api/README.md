# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-05-04-as-14_1777914637897.png" alt="Pling logo" width="28" height="28"> Pling: Universal API

Access public Pling content, category, license, recommendation, comment, event, and OCS configuration data through Pling's Open Collaboration Services API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pling/latest
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pling.com
- **Vendor API docs:** https://www.opendesktop.org/ocs-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Configuration](actions/get-api-configuration.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pling/latest/actions/get-api-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Content

| Action | Method | Description |
| --- | --- | --- |
| [Get Content](actions/get-content.md) | GET | Retrieves public content details from Pling. |
| [List Content](actions/list-content.md) | GET | Retrieves public content listings from Pling. |
| [List Content By Category](actions/list-content-by-category.md) | GET | Retrieves public content from Pling by category. |
| [List Content By User](actions/list-content-by-user.md) | GET | Retrieves public content from Pling by username. |
| [List Popular Content](actions/list-popular-content.md) | GET | Retrieves popular public content from Pling. |
| [Search Content](actions/search-content.md) | GET | Finds public content in Pling by search text. |

### Content Category

| Action | Method | Description |
| --- | --- | --- |
| [List Content Categories](actions/list-content-categories.md) | GET | Retrieves public content categories from Pling. |

### Content Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Content Comments](actions/list-content-comments.md) | GET | Retrieves public content comments from Pling. |

### Content Download

| Action | Method | Description |
| --- | --- | --- |
| [Get Content Download](actions/get-content-download.md) | GET | Retrieves a content download URL from Pling. |

### Ocs Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Get API Configuration](actions/get-api-configuration.md) | GET | Retrieves OCS API configuration details from Pling. |

