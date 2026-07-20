# Unkey: Apply multiple rate limit checks

Applies multiple rate limit checks in Unkey.

```
GET https://connect.mindcloud.co/v1/universal/unkey/latest/actions/apply-multiple-rate-limit-checks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/apply-multiple-rate-limit-checks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unkey/latest/actions/apply-multiple-rate-limit-checks?${params}`, {
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
      "data": {
        "limits": [
          [
            {}
          ]
        ],
        "passed": true
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
| `data.limits[]` | array<object> |  |
| `data.limits[].identifier` | string |  |
| `data.limits[].limit` | number |  |
| `data.limits[].namespace` | string |  |
| `data.limits[].overrideId` | string |  |
| `data.limits[].passed` | boolean |  |
| `data.limits[].remaining` | number |  |
| `data.limits[].reset` | number |  |
| `data.passed` | boolean |  |
| `meta` | object |  |
| `meta.requestId` | string |  |

## Native endpoint

Through the native Unkey API, this operation is `POST /v2/ratelimit.multiLimit` (base URL `https://api.unkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/apply-multiple-rate-limit-checks.md) for the provider-specific parameters and requirements.

