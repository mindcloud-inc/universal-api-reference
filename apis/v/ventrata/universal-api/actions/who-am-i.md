# Ventrata: Who Am I

Retrieves reseller connection details from Ventrata.

```
GET https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/who-am-i
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ventrata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/who-am-i?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/who-am-i?${params}`, {
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
      "connection": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "reseller": {
        "id": "string",
        "name": "Ava Chen"
      },
      "supplier": {
        "contact": {
          "address": "string",
          "email": "ava@example.com"
        },
        "endpoint": "string",
        "id": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connection.id` | string |  |
| `connection.name` | string |  |
| `connection.type` | string |  |
| `reseller.id` | string |  |
| `reseller.name` | string |  |
| `supplier.contact.address` | string |  |
| `supplier.contact.email` | string |  |
| `supplier.endpoint` | string |  |
| `supplier.id` | string |  |
| `supplier.name` | string |  |

## Native endpoint

Through the native Ventrata API, this operation is `GET octo/whoami` (base URL `https://api.ventrata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/who-am-i.md) for the provider-specific parameters and requirements.

