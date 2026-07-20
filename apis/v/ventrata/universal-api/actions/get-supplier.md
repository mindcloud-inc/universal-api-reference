# Ventrata: Get Supplier

Retrieves a supplier from Ventrata.

```
GET https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/get-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ventrata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/get-supplier?connectionId=$CONNECTION_ID&supplierId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "supplierId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/get-supplier?${params}`, {
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
| `supplierId` | string | yes | Supplier identifier from Ventrata. |

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

Through the native Ventrata API, this operation is `GET octo/suppliers/:supplierId` (base URL `https://api.ventrata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-supplier.md) for the provider-specific parameters and requirements.

