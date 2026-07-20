# EenvoudigFactureren: Get Payment Request

Retrieves a payment request from EenvoudigFactureren.

```
GET https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/get-payment-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EenvoudigFactureren `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/get-payment-request?connectionId=$CONNECTION_ID&paymentrequest_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paymentrequest_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/get-payment-request?${params}`, {
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
| `paymentrequest_id` | string | yes | EenvoudigFactureren payment request ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client_name": "Ava Chen",
      "date": "2026-05-07T12:00:00.000Z",
      "number": "string",
      "paymentrequest_id": 1,
      "status": "string",
      "total": 1,
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_name` | string |  |
| `date` | date |  |
| `number` | string |  |
| `paymentrequest_id` | number |  |
| `status` | string |  |
| `total` | number |  |
| `uri` | string |  |

## Native endpoint

Through the native EenvoudigFactureren API, this operation is `GET /paymentrequests/:paymentrequest_id` (base URL `https://eenvoudigfactureren.be/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-request.md) for the provider-specific parameters and requirements.

