# <img src="https://images.mindcloud.co/apps/icons/tabidoo_1774367948061.png" alt="Tabidoo logo" width="28" height="28"> Tabidoo: Universal API

Tabidoo is a low-code platform for building custom business apps around tables, records, workflows, and templates.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tabidoo/latest
- **Category:** IT Operations / Database
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tabidoo.cloud
- **Vendor API docs:** https://tabidoo.docs.apiary.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Apps](actions/list-apps.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tabidoo/latest/actions/list-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Create Development App From Production App](actions/create-development-app-from-production-app.md) | POST | Creates a development app from a production app in Tabidoo. |
| [Get App](actions/get-app.md) | GET | Retrieves an application from a Tabidoo workspace. |
| [List Apps](actions/list-apps.md) | GET | Retrieves applications from a Tabidoo workspace. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [List App Tables](actions/list-app-tables.md) | GET | Retrieves tables for an application in Tabidoo. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from the Tabidoo marketplace. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from the Tabidoo marketplace. |

