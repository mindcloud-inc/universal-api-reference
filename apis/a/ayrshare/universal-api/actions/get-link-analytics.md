# Ayrshare: Get Link Analytics

Retrieves short link analytics from Ayrshare.

```
GET https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/get-link-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/get-link-analytics?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/get-link-analytics?${params}`, {
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
| `id` | string | yes | Ayrshare short link ID to retrieve analytics for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clicks": 1,
      "code": 1,
      "countries": [
        {}
      ],
      "id": "string",
      "message": "string",
      "referrers": [
        {}
      ],
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clicks` | number | Total click count. |
| `code` | number | Ayrshare error code. |
| `countries` | array<object> | Click country breakdown. |
| `id` | string | Short link ID. |
| `message` | string | Analytics or error message. |
| `referrers` | array<object> | Click referrer breakdown. |
| `status` | string | Response status. |
| `url` | string | Destination URL. |

## Native endpoint

Through the native Ayrshare API, this operation is `GET /links/:id` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link-analytics.md) for the provider-specific parameters and requirements.

