# <img src="https://images.mindcloud.co/apps/icons/favicon_1776820425225.png" alt="Teletype App logo" width="28" height="28"> Teletype App: Universal API

Manage customer conversations, channels, operators, and project settings

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/teletypeApp/latest
- **Category:** Communication / Team Messaging
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://teletype.app/
- **Vendor API docs:** https://teletype.app/help/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Project Details](actions/get-project-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/get-project-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Appeal Category

| Action | Method | Description |
| --- | --- | --- |
| [List Appeal Categories](actions/list-appeal-categories.md) | GET | Retrieves appeal categories from Teletype App. |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [List Channels](actions/list-channels.md) | GET | Retrieves all channels from Teletype App. |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [List Clients](actions/list-clients.md) | GET | Retrieves all clients from Teletype App. |

### Dialog

| Action | Method | Description |
| --- | --- | --- |
| [List Dialogs](actions/list-dialogs.md) | GET | Retrieves all dialogs from Teletype App. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | GET | Retrieves all messages from Teletype App. |

### Message Template Catalog

| Action | Method | Description |
| --- | --- | --- |
| [Get Message Template Catalog](actions/get-message-template-catalog.md) | GET | Retrieves the message template catalog from Teletype App. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Details](actions/get-project-details.md) | GET | Retrieves project details from Teletype App. |

### Project Api Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Project API Status](actions/get-project-api-status.md) | GET | Retrieves project API status from Teletype App. |

### Project Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Balance](actions/get-project-balance.md) | GET | Retrieves project balance from Teletype App. |

### Project Operator

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Operators](actions/get-project-operators.md) | GET | Retrieves project operators from Teletype App. |

### Project Public Api Settings

| Action | Method | Description |
| --- | --- | --- |
| [Update Public API Settings](actions/update-public-api-settings.md) | PUT | Updates public API settings in Teletype App. |

### Project Tariff

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Tariff](actions/get-project-tariff.md) | GET | Retrieves project tariff from Teletype App. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves all tags from Teletype App. |

### Template Directory

| Action | Method | Description |
| --- | --- | --- |
| [List Template Directories](actions/list-template-directories.md) | GET | Retrieves template directories from Teletype App. |

