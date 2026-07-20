# Priority: Get Sales Order

Retrieves a sales order from Priority.

```
GET https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-sales-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-sales-order?connectionId=$CONNECTION_ID&ordName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ordName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-sales-order?${params}`, {
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
| `ordName` | string | yes | Priority sales order key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CDES": "string",
      "CURDATE": "2026-05-07T12:00:00.000Z",
      "CUSTNAME": "Ava Chen",
      "ORDNAME": "Ava Chen",
      "ORDSTATUSDES": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CDES` | string |  |
| `CURDATE` | date |  |
| `CUSTNAME` | string |  |
| `ORDNAME` | string |  |
| `ORDSTATUSDES` | string |  |

## Native endpoint

Through the native Priority API, this operation is `GET /ORDERS(ORDNAME=':ordName')` (base URL `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sales-order.md) for the provider-specific parameters and requirements.

