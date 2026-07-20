# QuickFile: Get Supplier



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-supplier?connectionId=$CONNECTION_ID&supplierId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "supplierId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-supplier?${params}`, {
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
| `supplierId` | number | yes | The QuickFile SupplierID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "email": "ava@example.com",
      "name": "Ava Chen",
      "phone": "string",
      "supplierId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number | Current supplier balance. |
| `email` | string | Primary supplier email. |
| `name` | string | Supplier display name. |
| `phone` | string | Primary supplier phone number. |
| `supplierId` | number | QuickFile supplier identifier. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /supplier/get` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-supplier.md) for the provider-specific parameters and requirements.

