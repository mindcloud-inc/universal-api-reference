# <img src="https://images.mindcloud.co/apps/icons/auphonic_1774557746535.png" alt="Auphonic logo" width="28" height="28"> Auphonic: Universal API

Process audio productions, manage presets, and integrate external workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/auphonic/latest
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://auphonic.com
- **Vendor API docs:** https://auphonic.com/help/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User Account Info](actions/get-current-user-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/get-current-user-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Audio Algorithm

| Action | Method | Description |
| --- | --- | --- |
| [Get Audio Algorithms](actions/get-audio-algorithms.md) | GET | Retrieves audio algorithms from Auphonic. |

### Info

| Action | Method | Description |
| --- | --- | --- |
| [Get API Information](actions/get-api-information.md) | GET | Retrieves API information from Auphonic. |

### Output File Format

| Action | Method | Description |
| --- | --- | --- |
| [Get Output File Formats](actions/get-output-file-formats.md) | GET | Retrieves output file formats from Auphonic. |

### Preset

| Action | Method | Description |
| --- | --- | --- |
| [Create Preset](actions/create-preset.md) | POST | Creates a new preset in Auphonic. |
| [Delete Preset](actions/delete-preset.md) | DELETE | Deletes an existing preset from Auphonic. |
| [Get Preset](actions/get-preset.md) | GET | Retrieves a preset from Auphonic. |
| [List Presets](actions/list-presets.md) | GET | Retrieves presets from Auphonic. |
| [Update Preset](actions/update-preset.md) | PUT | Updates an existing preset in Auphonic. |

### Production

| Action | Method | Description |
| --- | --- | --- |
| [Create Production](actions/create-production.md) | POST | Creates a new production in Auphonic. |
| [Delete Production](actions/delete-production.md) | DELETE | Deletes an existing production from Auphonic. |
| [Get Production](actions/get-production.md) | GET | Retrieves a production from Auphonic. |
| [List Productions](actions/list-productions.md) | GET | Retrieves productions from Auphonic. |
| [Stop Production](actions/stop-production.md) | PUT | Stops a production in Auphonic. |
| [Update Production](actions/update-production.md) | PUT | Updates an existing production in Auphonic. |

### Production Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Production Status](actions/get-production-status.md) | GET | Retrieves production status from Auphonic. |
| [Get Production Status Codes](actions/get-production-status-codes.md) | GET | Retrieves production status codes from Auphonic. |

### Production Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Delete Production Webhook](actions/delete-production-webhook.md) | DELETE | Deletes a production webhook from Auphonic. |
| [Get Production Webhook](actions/get-production-webhook.md) | GET | Retrieves a production webhook from Auphonic. |
| [Set Production Webhook](actions/set-production-webhook.md) | PUT | Sets a production webhook in Auphonic. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [List Services](actions/list-services.md) | GET | Retrieves external services from Auphonic. |

### Service Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Service Types](actions/get-service-types.md) | GET | Retrieves service types from Auphonic. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User Account Info](actions/get-current-user-account-info.md) | GET | Retrieves current user account info from Auphonic. |

