# Syften: Get Info

Retrieves account details and plan information from Syften.

```
GET https://connect.mindcloud.co/v1/universal/syften/latest/actions/get-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syften `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syften/latest/actions/get-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syften/latest/actions/get-info?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "plan": {},
      "quota_counters": {},
      "stats": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `name` | string |  |
| `plan` | object |  |
| `quota_counters` | object |  |
| `stats` | object |  |

## Native endpoint

Through the native Syften API, this operation is `POST /api/0.0/info/get` (base URL `https://syften.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-info.md) for the provider-specific parameters and requirements.

