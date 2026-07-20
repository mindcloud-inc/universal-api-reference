# <img src="https://images.mindcloud.co/apps/icons/ubi-bot_1776447515433.png" alt="UbiBot logo" width="28" height="28"> UbiBot: Universal API

Connect UbiBot environmental monitoring devices to list channels, inspect device metadata, review feed summaries, manage channel API keys, upload channel icons, import feed data, and send supported device commands.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ubiBot/latest
- **Category:** IT Operations / Observability
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ubibot.com
- **Vendor API docs:** https://www.ubibot.com/platform-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Supported Timezones](actions/list-supported-timezones.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/list-supported-timezones?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel](actions/get-channel.md) | GET | Retrieves a channel and its latest sensor data from UbiBot. |
| [List Channels](actions/list-channels.md) | GET | Retrieves available channels from UbiBot. |

### Channel Icon

| Action | Method | Description |
| --- | --- | --- |
| [Upload Channel Icon From Base64](actions/upload-channel-icon-from-base64.md) | PUT | Updates a channel icon from a Base64 string in UbiBot. |

### Channel Key

| Action | Method | Description |
| --- | --- | --- |
| [List Channel Keys](actions/list-channel-keys.md) | GET | Retrieves channel API keys from UbiBot. |

### Command

| Action | Method | Description |
| --- | --- | --- |
| [Add Command](actions/add-command.md) | POST | Creates a device command in UbiBot. |

### Feed Import

| Action | Method | Description |
| --- | --- | --- |
| [Import Feeds From CSV](actions/import-feeds-from-csv.md) | POST | Imports channel feeds from a CSV file in UbiBot. |

### Feed Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel Feed Summaries](actions/get-channel-feed-summaries.md) | GET | Retrieves channel feed summaries from UbiBot. |

### Read Key

| Action | Method | Description |
| --- | --- | --- |
| [Generate Channel Read Key](actions/generate-channel-read-key.md) | POST | Creates a channel read-only key in UbiBot. |

### Read-only Key

| Action | Method | Description |
| --- | --- | --- |
| [Delete Channel Read-only Key](actions/delete-channel-read-only-key.md) | DELETE | Deletes a channel read-only key from UbiBot. |

### Timezone

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Timezones](actions/list-supported-timezones.md) | GET | Retrieves supported platform timezones from UbiBot. |

