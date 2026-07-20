# Envoice: Get Order Details

Retrieves order details from Envoice.

```
GET https://connect.mindcloud.co/v1/universal/envoice/latest/actions/get-order-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/get-order-details?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoice/latest/actions/get-order-details?${params}`, {
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
| `id` | number | yes | Order identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Currency": {},
      "ErrorMessages": [
        "string"
      ],
      "Id": 1,
      "IsFaulted": true,
      "Items": [
        {}
      ],
      "Name": "Ava Chen",
      "Status": "string",
      "TotalAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Currency` | object | Currency details. |
| `ErrorMessages` | array<string> | Error messages returned by Envoice. |
| `Id` | number | Order identifier. |
| `IsFaulted` | boolean | Whether the request failed. |
| `Items` | array<object> | Order line items. |
| `Name` | string | Order name. |
| `Status` | string | Order status. |
| `TotalAmount` | number | Total order amount. |

## Native endpoint

Through the native Envoice API, this operation is `GET order/details` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-details.md) for the provider-specific parameters and requirements.

