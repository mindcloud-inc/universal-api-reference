# Notifyre SMS: Remove Contacts From Group

Removes contacts from a Notifyre group.

```
PUT https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/remove-contacts-from-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notifyre SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/remove-contacts-from-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts": "string",
  "groupId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/remove-contacts-from-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts": "string",
    "groupId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contacts` | list<string> | yes | Contacts to remove from the group. |
| `groupId` | string | yes | Group identifier for removal. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "removed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `removed` | boolean | Whether the contacts were removed from the group. |

## Native endpoint

Through the native Notifyre SMS API, this operation is `DELETE /addressbook/groups/contacts` (base URL `https://api.notifyre.com/20220711`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-contacts-from-group.md) for the provider-specific parameters and requirements.

