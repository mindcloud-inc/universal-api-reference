# Moodo & Moodo AIR: Get Interval Types

Retrieves interval types from Moodo & Moodo AIR.

```
GET https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/get-interval-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moodo & Moodo AIR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/get-interval-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/get-interval-types?${params}`, {
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
      "intervalTypes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `intervalTypes` | array<object> |  |

## Native endpoint

Through the native Moodo & Moodo AIR API, this operation is `GET /interval` (base URL `https://rest.moodo.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-interval-types.md) for the provider-specific parameters and requirements.

