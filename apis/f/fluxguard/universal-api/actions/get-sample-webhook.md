# Fluxguard: Get Sample Webhook

Retrieves a sample webhook payload from Fluxguard.

```
GET https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/get-sample-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluxguard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/get-sample-webhook?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/get-sample-webhook?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "capturedAt": "string",
      "comparisonType": "string",
      "diffUrl": "https://example.com",
      "fileBaseUrl": "https://example.com",
      "files": {},
      "orgId": "string",
      "page": {},
      "pageCategories": [
        {}
      ],
      "session": {},
      "site": {},
      "siteCategories": [
        {}
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capturedAt` | string | Capture timestamp in ISO-8601 format. |
| `comparisonType` | string | Comparison mode used for the sample. |
| `diffUrl` | string | Fluxguard diff view URL. |
| `fileBaseUrl` | string | Base URL for capture artifacts. |
| `files` | object | Capture and diff file references. |
| `orgId` | string | Fluxguard organization identifier. |
| `page` | object | Associated page information. |
| `pageCategories` | array<object> | Categories applied to the page. |
| `session` | object | Associated session information. |
| `site` | object | Associated site information. |
| `siteCategories` | array<object> | Categories applied to the site. |
| `url` | string | Monitored page URL included in the sample webhook. |

## Native endpoint

Through the native Fluxguard API, this operation is `GET /account/webhook/sample` (base URL `https://api.fluxguard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sample-webhook.md) for the provider-specific parameters and requirements.

