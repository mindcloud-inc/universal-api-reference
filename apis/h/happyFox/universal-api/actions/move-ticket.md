# HappyFox: Move Ticket

Moves a ticket to another category in HappyFox.

```
PUT https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/move-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/move-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketNumber": "string",
  "staffId": 1,
  "targetCategoryId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/move-ticket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketNumber": "string",
    "staffId": 1,
    "targetCategoryId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketNumber` | string | yes | HappyFox ticket number from the ticket display ID without the prefix. |
| `staffId` | number | yes |  |
| `targetCategoryId` | number | yes | Destination HappyFox category ID. |
| `moveNote` | string | no |  |
| `assignTo` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Confirmation message describing the ticket move result. |
| `statusCode` | number | HTTP-style status code returned by HappyFox after the move completes. |

## Native endpoint

Through the native HappyFox API, this operation is `POST /ticket/:ticket_number/move/` (base URL `https://{{credentials.accountDomain}}/api/1.1/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-ticket.md) for the provider-specific parameters and requirements.

