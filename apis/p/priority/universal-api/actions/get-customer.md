# Priority: Get Customer

Retrieves a customer from Priority.

```
GET https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-customer?connectionId=$CONNECTION_ID&custName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "custName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-customer?${params}`, {
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
| `custName` | string | yes | Priority customer key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CUSTDES": "string",
      "CUSTNAME": "Ava Chen",
      "EMAIL": "ava@example.com",
      "PHONE": "string",
      "STATDES": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CUSTDES` | string |  |
| `CUSTNAME` | string |  |
| `EMAIL` | string |  |
| `PHONE` | string |  |
| `STATDES` | string |  |

## Native endpoint

Through the native Priority API, this operation is `GET /CUSTOMERS(CUSTNAME=':custName')` (base URL `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

