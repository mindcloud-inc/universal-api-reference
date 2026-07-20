# Priority: Get Purchase Order

Retrieves a purchase order from Priority.

```
GET https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-purchase-order?connectionId=$CONNECTION_ID&ordName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ordName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-purchase-order?${params}`, {
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
| `ordName` | string | yes | Priority purchase order key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CDES": "string",
      "CURDATE": "2026-05-07T12:00:00.000Z",
      "ORDNAME": "Ava Chen",
      "STATDES": "string",
      "SUPNAME": "Ava Chen"
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
| `ORDNAME` | string |  |
| `STATDES` | string |  |
| `SUPNAME` | string |  |

## Native endpoint

Through the native Priority API, this operation is `GET /PORDERS(ORDNAME=':ordName')` (base URL `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-purchase-order.md) for the provider-specific parameters and requirements.

