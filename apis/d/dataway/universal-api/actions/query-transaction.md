# Dataway: Query Transaction

Retrieves transaction details from Dataway by client reference.

```
GET https://connect.mindcloud.co/v1/universal/dataway/latest/actions/query-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dataway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataway/latest/actions/query-transaction?connectionId=$CONNECTION_ID&reference=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reference": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataway/latest/actions/query-transaction?${params}`, {
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
| `reference` | string | yes | Client reference to query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "amount": 1,
        "commission": 1,
        "date": "2026-05-07T12:00:00.000Z",
        "externalReference": "string",
        "extras": {},
        "reference": "string",
        "status": "string",
        "title": "string"
      },
      "responseCode": "string",
      "responseDescription": "string",
      "responseMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Queried transaction result. |
| `data.amount` | number | Transaction amount when returned numerically. |
| `data.commission` | number | Provider commission when returned numerically. |
| `data.date` | date | Transaction date. |
| `data.externalReference` | string | Client-supplied reference echoed by the provider. |
| `data.extras` | object | Provider-specific extras object. |
| `data.reference` | string | Provider reference when returned. |
| `data.status` | string | Transaction status. |
| `data.title` | string | Transaction title when returned. |
| `responseCode` | string | Provider response code. |
| `responseDescription` | string | Provider response description. |
| `responseMessage` | string | Provider response message. |

## Native endpoint

Through the native Dataway API, this operation is `POST /query-transaction` (base URL `https://datawayapp.com/vendor`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-transaction.md) for the provider-specific parameters and requirements.

