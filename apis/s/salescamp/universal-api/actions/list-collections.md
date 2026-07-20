# Salescamp: List Collections



```
GET https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/list-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salescamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/list-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/list-collections?${params}`, {
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
      "fieldCounts": 1,
      "id": "string",
      "isSystem": true,
      "label": "string",
      "name": "Ava Chen",
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fieldCounts` | number |  |
| `id` | string |  |
| `isSystem` | boolean |  |
| `label` | string |  |
| `name` | string |  |
| `type` | number |  |

## Native endpoint

Through the native Salescamp API, this operation is `GET /v1/collections` (base URL `https://api.salescamp.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-collections.md) for the provider-specific parameters and requirements.

