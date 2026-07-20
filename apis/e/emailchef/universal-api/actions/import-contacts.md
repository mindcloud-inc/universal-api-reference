# Emailchef: Import Contacts

Imports contacts into an Emailchef list.

```
POST https://connect.mindcloud.co/v1/universal/emailchef/latest/actions/import-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emailchef `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emailchef/latest/actions/import-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emailchef/latest/actions/import-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | The Emailchef list ID. |
| `instanceIn.contacts[]` | array<array> | no |  |
| `instanceIn.notificationLink` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Emailchef API returns.

## Native endpoint

Through the native Emailchef API, this operation is `POST lists/:list_id/import` (base URL `https://app.emailchef.com/apps/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-contacts.md) for the provider-specific parameters and requirements.

