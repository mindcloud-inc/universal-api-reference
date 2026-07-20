# Mighty Tix: Update Session Ticket Type

Updates an existing session ticket type in Mighty Tix.

```
PUT https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/update-session-ticket-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Tix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/update-session-ticket-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.input": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/update-session-ticket-type', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.input": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.input` | object | yes | UpdateOneSessionTicketTypeInput object from the Mighty Tix Admin GraphQL docs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bookingFee": 1,
      "capacity": 1,
      "enabled": true,
      "price": 1,
      "sessionId": "string",
      "ticketTypeId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bookingFee` | number |  |
| `capacity` | number |  |
| `enabled` | boolean |  |
| `price` | number |  |
| `sessionId` | string |  |
| `ticketTypeId` | string |  |

## Native endpoint

Through the native Mighty Tix API, this operation is `POST admin-api/graphql` (base URL `https://mindcloudmttix260403.mightytix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-session-ticket-type.md) for the provider-specific parameters and requirements.

