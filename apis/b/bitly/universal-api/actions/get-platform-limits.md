# Bitly: Get Platform Limits

Retrieves platform limits from your Bitly account.

```
GET https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-platform-limits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-platform-limits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-platform-limits?${params}`, {
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
| `path` | string | no | Filter platform limits to one API path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "platformLimits": [
        {
          "endpoint": "string",
          "methods": [
            {
              "count": 1,
              "limit": 1,
              "name": "Ava Chen"
            }
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `platformLimits[].endpoint` | string |  |
| `platformLimits[].methods[].count` | number |  |
| `platformLimits[].methods[].limit` | number |  |
| `platformLimits[].methods[].name` | string |  |

## Native endpoint

Through the native Bitly API, this operation is `GET /user/platform_limits` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-platform-limits.md) for the provider-specific parameters and requirements.

