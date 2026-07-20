# Emailchef: Create Contact

Creates a new contact in Emailchef.

```
POST https://connect.mindcloud.co/v1/universal/emailchef/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emailchef `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emailchef/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "instanceIn.listId": "string",
  "instanceIn.email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emailchef/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "instanceIn.listId": "string",
    "instanceIn.email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `instanceIn.listId` | string | yes |  |
| `instanceIn.email` | string | yes |  |
| `instanceIn.status` | string | no |  |
| `instanceIn.firstname` | string | no |  |
| `instanceIn.lastname` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Emailchef API returns.

## Native endpoint

Through the native Emailchef API, this operation is `POST contacts` (base URL `https://app.emailchef.com/apps/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

