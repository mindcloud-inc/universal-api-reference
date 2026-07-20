# Emailchef: Update List

Updates an existing mailing list in Emailchef.

```
PUT https://connect.mindcloud.co/v1/universal/emailchef/latest/actions/update-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emailchef `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/emailchef/latest/actions/update-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emailchef/latest/actions/update-list', {
  method: 'PUT',
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
| `instanceIn.listName` | string | no | The updated name for the list. |
| `instanceIn.listDescription` | string | no | The updated description for the list. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Emailchef API returns.

## Native endpoint

Through the native Emailchef API, this operation is `PUT lists/:list_id` (base URL `https://app.emailchef.com/apps/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-list.md) for the provider-specific parameters and requirements.

