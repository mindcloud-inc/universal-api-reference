# Mighty Tix: Get Session Ticket Type

Retrieves a session ticket type from Mighty Tix.

```
GET https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/get-session-ticket-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Tix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/get-session-ticket-type?connectionId=$CONNECTION_ID&variables.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/get-session-ticket-type?${params}`, {
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
| `variables.id` | string | yes | Session ticket type ID from the Mighty Tix Admin GraphQL docs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bookingFee": 1,
      "capacity": 1,
      "countIssued": 1,
      "countPending": 1,
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
| `countIssued` | number |  |
| `countPending` | number |  |
| `enabled` | boolean |  |
| `price` | number |  |
| `sessionId` | string |  |
| `ticketTypeId` | string |  |

## Native endpoint

Through the native Mighty Tix API, this operation is `POST admin-api/graphql` (base URL `https://mindcloudmttix260403.mightytix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session-ticket-type.md) for the provider-specific parameters and requirements.

