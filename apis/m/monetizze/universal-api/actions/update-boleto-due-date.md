# Monetizze: Update Boleto Due Date

Updates a boleto due date in Monetizze.

```
PUT https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/update-boleto-due-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monetizze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/update-boleto-due-date" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transaction": 1,
  "dueDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/update-boleto-due-date', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transaction": 1,
    "dueDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transaction` | number | yes | Sale code whose boleto due date should be updated. |
| `dueDate` | string | yes | New boleto due date in yyyy-mm-dd format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "status": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Provider error message when the boleto update fails. |
| `status` | number | HTTP-style status returned by Monetizze for the boleto update. |
| `url` | string | Boleto URL returned by Monetizze when applicable. |

## Native endpoint

Through the native Monetizze API, this operation is `POST /boleto` (base URL `https://api.monetizze.com.br/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-boleto-due-date.md) for the provider-specific parameters and requirements.

