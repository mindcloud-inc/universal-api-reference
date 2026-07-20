# Intruder: List Targets



```
GET https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-targets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intruder `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-targets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-targets?${params}`, {
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
      "address": "string",
      "displayAddress": "string",
      "hasApiSchemas": true,
      "hasAuthentications": true,
      "id": 1,
      "licenseType": "string",
      "tags": [
        "string"
      ],
      "targetStatus": "string",
      "targetType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `displayAddress` | string |  |
| `hasApiSchemas` | boolean |  |
| `hasAuthentications` | boolean |  |
| `id` | number |  |
| `licenseType` | string |  |
| `tags` | array<string> |  |
| `targetStatus` | string |  |
| `targetType` | string |  |

## Native endpoint

Through the native Intruder API, this operation is `GET /targets/` (base URL `https://api.intruder.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-targets.md) for the provider-specific parameters and requirements.

