# <img src="https://images.mindcloud.co/apps/icons/cropped-time-buzzer-symbol-3-32x32_1774304606340.png" alt="timeBuzzer logo" width="28" height="28"> timeBuzzer: Universal API

Track time, manage projects, tasks, and customers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/timeBuzzer/latest
- **Category:** Productivity / Project Management
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://timebuzzer.com
- **Vendor API docs:** https://my.timebuzzer.com/doc/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Account](actions/get-my-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/get-my-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get My Account](actions/get-my-account.md) | GET |  |

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | POST |  |
| [Delete Activity](actions/delete-activity.md) | DELETE |  |
| [List Activities](actions/list-activities.md) | GET |  |
| [Search Activities](actions/search-activities.md) | GET |  |
| [Update Activity](actions/update-activity.md) | PUT |  |

### Layer

| Action | Method | Description |
| --- | --- | --- |
| [List Layers](actions/list-layers.md) | GET |  |

### Tile

| Action | Method | Description |
| --- | --- | --- |
| [Create Tile](actions/create-tile.md) | POST |  |
| [Get Tile](actions/get-tile.md) | GET |  |
| [List Tiles](actions/list-tiles.md) | GET |  |
| [Search Tiles](actions/search-tiles.md) | GET |  |
| [Update Tile](actions/update-tile.md) | PUT |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Configuration](actions/create-webhook-configuration.md) | POST |  |
| [Delete Webhook Configuration](actions/delete-webhook-configuration.md) | DELETE |  |
| [Delete Webhook Configuration By URL](actions/delete-webhook-configuration-by-url.md) | DELETE |  |
| [List Webhook Configurations](actions/list-webhook-configurations.md) | GET |  |
| [Update Webhook Configuration](actions/update-webhook-configuration.md) | PUT |  |

