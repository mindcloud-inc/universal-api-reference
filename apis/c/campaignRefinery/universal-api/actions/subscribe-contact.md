# Campaign Refinery: Subscribe Contact

Subscribes an existing contact in Campaign Refinery.

```
POST https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/subscribe-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Refinery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/subscribe-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/subscribe-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The contact's email address. |
| `firstName` | string | no | The contact's first name. |
| `lastName` | string | no | The contact's last name. |
| `tags` | string | no | One or more tag UUIDs separated by commas. Accepts multiple values in one string, delimited by `,`. |
| `sequences` | string | no | One or more sequence UUIDs separated by commas. Accepts multiple values in one string, delimited by `,`. |
| `formId` | string | no | The form UUID to associate with the contact. |
| `goalId` | string | no | The goal UUID to mark complete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Campaign Refinery API returns.

## Native endpoint

Through the native Campaign Refinery API, this operation is `POST /contacts/subscribe` (base URL `https://app.campaignrefinery.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-contact.md) for the provider-specific parameters and requirements.

