# <img src="https://images.mindcloud.co/apps/icons/idkhll1p0h-1776372894554_1776372899363.png" alt="Rachio Smart Lighting Controller logo" width="28" height="28"> Rachio Smart Lighting Controller: Universal API

Manage Rachio smart lighting zones, scenes, and programs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rachioSmartLightingController/latest
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rachio.com/products/smart-lighting-controller
- **Vendor API docs:** https://rachio.readme.io/reference/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Person ID](actions/get-current-person-id.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rachioSmartLightingController/latest/actions/get-current-person-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Update Lighting Controller](actions/update-lighting-controller.md) | PUT |  |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Lighting Zone Group](actions/create-lighting-zone-group.md) | POST |  |
| [Delete Lighting Zone Group](actions/delete-lighting-zone-group.md) | DELETE |  |
| [Update Lighting Zone Group](actions/update-lighting-zone-group.md) | PUT |  |

### Lighting Area

| Action | Method | Description |
| --- | --- | --- |
| [List Lighting Areas](actions/list-lighting-areas.md) | GET |  |

### Lighting Program

| Action | Method | Description |
| --- | --- | --- |
| [List Lighting Programs](actions/list-lighting-programs.md) | GET |  |

### Lighting Zone

| Action | Method | Description |
| --- | --- | --- |
| [List Lighting Zones](actions/list-lighting-zones.md) | GET |  |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Person Details](actions/get-current-person-details.md) | GET |  |
| [Get Current Person ID](actions/get-current-person-id.md) | GET |  |

### Programs

| Action | Method | Description |
| --- | --- | --- |
| [Create Lighting Program](actions/create-lighting-program.md) | POST |  |
| [Delete Lighting Program](actions/delete-lighting-program.md) | DELETE |  |
| [Update Lighting Program](actions/update-lighting-program.md) | PUT |  |

### Property

| Action | Method | Description |
| --- | --- | --- |
| [List Properties](actions/list-properties.md) | GET |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Activate Lighting Scene](actions/activate-lighting-scene.md) | PUT |  |
| [Create Lighting Scene](actions/create-lighting-scene.md) | POST |  |
| [Deactivate Lighting Scene](actions/deactivate-lighting-scene.md) | PUT |  |
| [Delete Lighting Scene](actions/delete-lighting-scene.md) | DELETE |  |
| [Set Lighting Zone Desired Dimming Settings](actions/set-lighting-zone-desired-dimming-settings.md) | PUT |  |
| [Set Lighting Zone Dimming Levels](actions/set-lighting-zone-dimming-levels.md) | PUT |  |
| [Set Lighting Zone States](actions/set-lighting-zone-states.md) | PUT |  |
| [Update Lighting Scene](actions/update-lighting-scene.md) | PUT |  |
| [Update Lighting Zone](actions/update-lighting-zone.md) | PUT |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete All Webhooks](actions/delete-all-webhooks.md) | DELETE |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [Update Webhook](actions/update-webhook.md) | PUT |  |

### Webhook Event Type

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Event Types](actions/list-webhook-event-types.md) | GET |  |

