# <img src="https://images.mindcloud.co/apps/icons/xmhz-u9ved-gs-iz3wryl-mz-lrc8f0c_1777309298562.png" alt="ShortPen logo" width="28" height="28"> ShortPen: Universal API

Create, track, and manage branded links and QR codes

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shortPen/latest
- **Category:** Marketing
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://shortpen.com
- **Vendor API docs:** https://shortpen.com/docs/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortPen/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Authenticated User

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET | Retrieves authenticated user details from ShortPen. |

### Click Analytics Event

| Action | Method | Description |
| --- | --- | --- |
| [List Click Analytics](actions/list-click-analytics.md) | GET | Retrieves click analytics from ShortPen for a date range. |
| [List Link Click Analytics](actions/list-link-click-analytics.md) | GET | Retrieves click analytics for one ShortPen link by date range. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [List Domains](actions/list-domains.md) | GET | Retrieves available short-link domains from ShortPen. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from ShortPen for a specific workspace. |

### Health Check

| Action | Method | Description |
| --- | --- | --- |
| [Check API Health](actions/check-api-health.md) | GET | Checks connectivity to the ShortPen API. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Link](actions/create-link.md) | POST | Creates a new link in ShortPen. |
| [List Links](actions/list-links.md) | GET | Retrieves links from ShortPen for a specific workspace. |
| [Update Link](actions/update-link.md) | PUT | Updates an existing link in ShortPen. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves authenticated organization details from ShortPen. |

### Pixel

| Action | Method | Description |
| --- | --- | --- |
| [List Pixels](actions/list-pixels.md) | GET | Retrieves available tracking pixels from ShortPen. |

