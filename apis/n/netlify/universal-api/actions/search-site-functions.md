# Netlify: Search Site Functions



```
GET https://connect.mindcloud.co/v1/universal/netlify/latest/actions/search-site-functions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Netlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/search-site-functions?connectionId=$CONNECTION_ID&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netlify/latest/actions/search-site-functions?${params}`, {
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
| `siteId` | list<string> | yes | The Netlify site ID. |
| `filter` | string | no | Filter functions for the site. Example: `ssr`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branch": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "functions": [
        {}
      ],
      "id": "string",
      "logType": "string",
      "provider": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branch` | string |  |
| `createdAt` | date |  |
| `functions` | array<object> |  |
| `id` | string |  |
| `logType` | string |  |
| `provider` | string |  |

## Native endpoint

Through the native Netlify API, this operation is `GET /sites/:site_id/functions` (base URL `https://api.netlify.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-site-functions.md) for the provider-specific parameters and requirements.

