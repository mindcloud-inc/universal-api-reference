# Fluxguard: Get Page Data

Retrieves data for a monitored page from Fluxguard.

```
GET https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/get-page-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluxguard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/get-page-data?connectionId=$CONNECTION_ID&siteId=string&sessionId=string&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "string",
  "sessionId": "string",
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/get-page-data?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | string | yes |  |
| `sessionId` | string | yes |  |
| `pageId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "orgId": "string",
      "pageCategories": [
        {}
      ],
      "path": "string",
      "session": {},
      "site": {},
      "siteCategories": [
        {}
      ],
      "status": "string",
      "url": "https://example.com",
      "versions": 1,
      "versionsKept": 1,
      "viewUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `id` | string |  |
| `orgId` | string |  |
| `pageCategories` | array<object> |  |
| `path` | string |  |
| `session` | object |  |
| `site` | object |  |
| `siteCategories` | array<object> |  |
| `status` | string |  |
| `url` | string |  |
| `versions` | number |  |
| `versionsKept` | number |  |
| `viewUrl` | string |  |

## Native endpoint

Through the native Fluxguard API, this operation is `GET /site/:siteId/session/:sessionId/page/:pageId` (base URL `https://api.fluxguard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-data.md) for the provider-specific parameters and requirements.

