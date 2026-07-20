# UbiBot: Native API Reference

A consolidated summary of UbiBot's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://www.ubibot.com/platform-api/
- **API base URL:** `https://webapi.ubibot.com`

## Authentication

### Account Key

UbiBot account-level authentication using the account_key from Web Console > Account > Security. The key is stored in MindCloud as the standard API key credential and sent to UbiBot as the account_key query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.ubibot.com/platform-api/1232/quick-start/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_key` | query | `string` | yes | UbiBot account_key query parameter required by the Platform API. |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Command](actions/add-command.md) | `POST /channels/:channelId/commands` | [docs](https://www.ubibot.com/platform-api/1987/add-command/) |
| [Delete Channel Read-only Key](actions/delete-channel-read-only-key.md) | `POST /channels/:channelId/api_keys` | [docs](https://www.ubibot.com/app-platform-api/8223/delete-channel-read-only-key/) |
| [Generate Channel Read Key](actions/generate-channel-read-key.md) | `POST /channels/:channelId/api_keys` | [docs](https://www.ubibot.com/app-platform-api/8225/generate-channel-read-only-key/) |
| [Get Channel](actions/get-channel.md) | `GET /channels/:channelId` | [docs](https://www.ubibot.com/platform-api/1174/view-channel/) |
| [Get Channel Feed Summaries](actions/get-channel-feed-summaries.md) | `GET /channels/:channelId/summary.json` | [docs](https://www.ubibot.com/platform-api/2735/get-channel-feed-summaries/) |
| [Import Feeds From CSV](actions/import-feeds-from-csv.md) | `POST /update.csv` | [docs](https://www.ubibot.com/platform-api/1213/csv-import-channel-feed/) |
| [List Channel Keys](actions/list-channel-keys.md) | `GET /channels/:channelId/api_keys` | [docs](https://www.ubibot.com/platform-api/1181/list-channel-api-keys/) |
| [List Channels](actions/list-channels.md) | `GET /channels` | [docs](https://www.ubibot.com/platform-api/1113/get-channels/) |
| [List Supported Timezones](actions/list-supported-timezones.md) | `GET /constants/timezones` | [docs](https://www.ubibot.com/platform-api/1232/quick-start/) |
| [Upload Channel Icon From Base64](actions/upload-channel-icon-from-base64.md) | `POST /channels/:channelId/device/upload_icon_base64` | [docs](https://www.ubibot.com/platform-api/1885/upload-channel-icon-base64/) |
