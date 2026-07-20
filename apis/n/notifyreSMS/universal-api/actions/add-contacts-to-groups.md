# Notifyre SMS: Add Contacts To Groups

Adds contacts to groups in Notifyre.

```
PUT https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/add-contacts-to-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notifyre SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/add-contacts-to-groups" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts": "string",
  "groups": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/add-contacts-to-groups', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts": "string",
    "groups": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contacts` | list<string> | yes | Contacts to add to groups. |
| `groups` | list<string> | yes | Target groups. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "added": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `added` | boolean | Whether the contacts were added to the groups. |

## Native endpoint

Through the native Notifyre SMS API, this operation is `POST /addressbook/groups/contacts` (base URL `https://api.notifyre.com/20220711`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contacts-to-groups.md) for the provider-specific parameters and requirements.

