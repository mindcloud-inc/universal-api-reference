# SMSEdge: Create Contact

Creates a new contact in a SMSEdge list.

```
POST https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSEdge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list_id": 1,
  "number": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list_id": 1,
    "number": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `birthday` | string | no | Birthday in year-month-day format |
| `country` | string | no | Country ISO or name for localized formatting |
| `country_id` | number | no | ID of country when the phone number is local format |
| `email` | string | no | E-mail of recipient |
| `gender` | string | no | Recipient gender using the provider's accepted values |
| `list_id` | number | yes | Number will be added to list with this ID |
| `lname` | string | no | Last name of recipient |
| `name` | string | no | Name of recipient |
| `number` | string | yes | Phone number of recipient |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMSEdge API returns.

## Native endpoint

Through the native SMSEdge API, this operation is `POST /numbers/create/` (base URL `https://api.smsedge.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

