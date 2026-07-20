# Unkey: Set ratelimit override

Sets a rate limit override in Unkey.

```
PUT https://connect.mindcloud.co/v1/universal/unkey/latest/actions/set-ratelimit-override
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/set-ratelimit-override" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "duration": 1,
  "identifier": "string",
  "limit": 1,
  "namespace": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unkey/latest/actions/set-ratelimit-override', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "duration": 1,
    "identifier": "string",
    "limit": 1,
    "namespace": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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
        "overrideId": "string"
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
| `data.overrideId` | string |  |
| `meta` | object |  |
| `meta.requestId` | string |  |

## Native endpoint

Through the native Unkey API, this operation is `POST /v2/ratelimit.setOverride` (base URL `https://api.unkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-ratelimit-override.md) for the provider-specific parameters and requirements.

