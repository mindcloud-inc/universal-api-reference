# Dachser: Get Delivery Notes

Retrieves delivery notes from Dachser by reference or date.

```
GET https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-delivery-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dachser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-delivery-notes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-delivery-notes?${params}`, {
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
| `purchaseOrderNumber` | string | no | Purchase order number. |
| `referenceNumber1` | string | no | First delivery note reference number. |
| `referenceNumber2` | string | no | Second delivery note reference number. |
| `referenceNumber3` | string | no | Third delivery note reference number. |
| `deliveryOrderDate` | date | no | Delivery order date. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `acceptLanguage` | string | no | Optional language sent as the Accept-Language header. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deliveryOrder": [
        {}
      ],
      "documents": [
        {}
      ],
      "id": "string",
      "references": [
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
| `deliveryOrder` | array<object> |  |
| `documents` | array<object> |  |
| `id` | string |  |
| `references` | array<object> |  |

## Native endpoint

Through the native Dachser API, this operation is `GET /rest/v2/deliverynotes` (base URL `https://api-gateway.dachser.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-delivery-notes.md) for the provider-specific parameters and requirements.

