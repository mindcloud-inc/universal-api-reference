# Ventrata: List Suppliers

Retrieves suppliers from Ventrata.

```
GET https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/list-suppliers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ventrata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/list-suppliers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/list-suppliers?${params}`, {
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
      "contact": {
        "address": "string",
        "email": "ava@example.com"
      },
      "endpoint": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact.address` | string |  |
| `contact.email` | string |  |
| `endpoint` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Ventrata API, this operation is `GET octo/suppliers` (base URL `https://api.ventrata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-suppliers.md) for the provider-specific parameters and requirements.

