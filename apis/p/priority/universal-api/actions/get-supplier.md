# Priority: Get Supplier

Retrieves a supplier from Priority.

```
GET https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-supplier?connectionId=$CONNECTION_ID&supName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "supName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-supplier?${params}`, {
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
| `supName` | string | yes | Priority supplier key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "EMAIL": "ava@example.com",
      "PHONE": "string",
      "STATDES": "string",
      "SUPDES": "string",
      "SUPNAME": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `EMAIL` | string |  |
| `PHONE` | string |  |
| `STATDES` | string |  |
| `SUPDES` | string |  |
| `SUPNAME` | string |  |

## Native endpoint

Through the native Priority API, this operation is `GET /SUPPLIERS(SUPNAME=':supName')` (base URL `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-supplier.md) for the provider-specific parameters and requirements.

