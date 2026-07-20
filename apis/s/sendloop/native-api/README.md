# Sendloop: Native API Reference

A consolidated summary of Sendloop's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://chmyos.notion.site/API-reference-eaa4fa70940b4daa928bde3dbf2245a5
- **API base URL:** `https://{subdomain}.sendloop.com/api/v3`

## Authentication

### API Key

Use your Sendloop API key to authenticate API requests.

### Credentials

- **API Key:** `apiKey` · required
- **Account Subdomain:** `subdomain` · required · Your Sendloop account subdomain from https://<subdomain>.sendloop.com, used to build the API URL.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://chmyos.notion.site/API-reference-eaa4fa70940b4daa928bde3dbf2245a5)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | `POST /campaign.create/json` | [docs](https://chmyos.notion.site/Create-a-Campaign-v2-0-937e18e29f374c7da5233e1762f81526) |
| [Create List](actions/create-list.md) | `POST /list.create/json` | [docs](https://chmyos.notion.site/Create-a-List-84fdbbb13cfc4a21a65def3e4ea372c9) |
| [Get Account Info](actions/get-account-info.md) | `POST /account.info.get/json` | [docs](https://chmyos.notion.site/Get-Account-Info-c0ed6e74d95c47609b92225643c5415b) |
| [Get Campaign](actions/get-campaign.md) | `POST /campaign.get/json` | [docs](https://chmyos.notion.site/Get-a-Campaign-f97ba801912044c0bf02cc46ba11d3ee) |
| [Get List](actions/get-list.md) | `POST /list.get/json` | [docs](https://chmyos.notion.site/Get-a-List-cc01af17aac64de9a6fecd9a82359815) |
| [Get List Settings](actions/get-list-settings.md) | `POST /list.settings.get/json` | [docs](https://chmyos.notion.site/Get-List-Settings-9117159181d14d5c8be9007737957470) |
| [Get Subscriber](actions/get-subscriber.md) | `POST /subscriber.get/json` | [docs](https://chmyos.notion.site/Get-a-Subscriber-2609e6e0fd7c4b0caa30da3cd6e13c15) |
| [Import Subscribers](actions/import-subscribers.md) | `POST /subscriber.import/json` | [docs](https://chmyos.notion.site/Import-Subscribers-eb12e964eb804901a180f084a2c77c0c) |
| [List Campaigns](actions/list-campaigns.md) | `POST /campaign.getlist/json` | [docs](https://chmyos.notion.site/Get-Campaign-List-555b08159aa64d8cb16ff9e9eb5985a8) |
| [List Campaigns by Status](actions/list-campaigns-by-status.md) | `POST /campaign.getlistbystatus/json` | [docs](https://chmyos.notion.site/Get-Campaign-List-By-Status-a6c63b9183544388994012eb22ad0e94) |
| [List Lists](actions/list-lists.md) | `POST /list.getlist/json` | [docs](https://chmyos.notion.site/Get-Lists-fbd3cc05ee3540d09387f9bae45dae6e) |
| [List Subscribers](actions/list-subscribers.md) | `POST /subscriber.browse/json` | [docs](https://chmyos.notion.site/List-Subscribers-0a8cd681380d428cbe0f217dc151d89a) |
| [Search Subscribers](actions/search-subscribers.md) | `POST /subscriber.search/json` | [docs](https://chmyos.notion.site/Search-Subscribers-5e9d41998a5945d4912d9bb1cd228a51) |
| [Subscribe Email Address](actions/subscribe-email-address.md) | `POST /subscriber.subscribe/json` | [docs](https://chmyos.notion.site/Subscribe-an-Email-Address-24b06739a31c42a199d8888984bb7b1b) |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | `POST /subscriber.unsubscribe/json` | [docs](https://chmyos.notion.site/Unsubscribe-a-Subscriber-39e13dd994fd48ce8f4da068f5ac39c9) |
| [Update Account Info](actions/update-account-info.md) | `POST /account.info.update/json` | [docs](https://chmyos.notion.site/Update-Account-Info-d83e5542ee4147ec9e27dd95a1bad17e) |
| [Update Campaign](actions/update-campaign.md) | `POST /campaign.update/json` | [docs](https://chmyos.notion.site/Update-details-of-a-Campaign-89e59c4024244874944093c47fb61039) |
| [Update List](actions/update-list.md) | `POST /list.update/json` | [docs](https://chmyos.notion.site/Update-a-List-71043bfda0394f2fa129cf24c7453512) |
| [Update List Settings](actions/update-list-settings.md) | `POST /list.settings.update/json` | [docs](https://chmyos.notion.site/Update-List-Settings-0deb49bea02d43c6a27779648ecaa3e3) |
| [Update Subscriber](actions/update-subscriber.md) | `POST /subscriber.update/json` | [docs](https://chmyos.notion.site/Update-a-Subscriber-efc3bdade57e448cb862ce6924cad424) |
