# Ordoro: Get Packing List by ID

Retrieves a packing list from Ordoro by ID.

```
GET https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/get-packing-list-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ordoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/get-packing-list-by-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/get-packing-list-by-id?${params}`, {
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Ordoro API, this operation is `GET /packing_list/{packing_list_id}/` (base URL `https://api.ordoro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-packing-list-by-id.md) for the provider-specific parameters and requirements.

