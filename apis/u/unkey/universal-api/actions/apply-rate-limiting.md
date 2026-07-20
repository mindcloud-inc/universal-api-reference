# Unkey: Apply rate limiting

Applies a rate limit check in Unkey.

```
GET https://connect.mindcloud.co/v1/universal/unkey/latest/actions/apply-rate-limiting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/apply-rate-limiting?connectionId=$CONNECTION_ID&duration=1&identifier=string&limit=1&namespace=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "duration": "1",
  "identifier": "string",
  "limit": "1",
  "namespace": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unkey/latest/actions/apply-rate-limiting?${params}`, {
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
| `duration` | number | yes |  |
| `identifier` | string | yes |  |
| `limit` | number | yes |  |
| `namespace` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "limit": 1,
        "overrideId": "string",
        "remaining": 1,
        "reset": 1,
        "success": true
      },
      "meta": {
        "requestId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.limit` | number |  |
| `data.overrideId` | string |  |
| `data.remaining` | number |  |
| `data.reset` | number |  |
| `data.success` | boolean |  |
| `meta` | object |  |
| `meta.requestId` | string |  |

## Native endpoint

Through the native Unkey API, this operation is `POST /v2/ratelimit.limit` (base URL `https://api.unkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/apply-rate-limiting.md) for the provider-specific parameters and requirements.

