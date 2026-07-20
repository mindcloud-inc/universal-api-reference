# Mighty Tix: Delete Session Ticket Type

Deletes an existing session ticket type from Mighty Tix.

```
DELETE https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/delete-session-ticket-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Tix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/delete-session-ticket-type?connectionId=$CONNECTION_ID&variables.input=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.input": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/delete-session-ticket-type?${params}`, {
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
| `variables.input` | string | no | DeleteOneSessionTicketTypeInput object from the Mighty Tix Admin GraphQL docs. |
| `variables.input` | object | yes | DeleteOneSessionTicketTypeInput object from the Mighty Tix Admin GraphQL docs. |

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

Through the native Mighty Tix API, this operation is `POST admin-api/graphql` (base URL `https://mindcloudmttix260403.mightytix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-session-ticket-type.md) for the provider-specific parameters and requirements.

