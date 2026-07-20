# HappyFox: Remove Contacts from Contact Group

Removes contacts from a HappyFox contact group.

```
PUT https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/remove-contacts-from-contact-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/remove-contacts-from-contact-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactGroupId": "string",
  "contacts[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/remove-contacts-from-contact-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactGroupId": "string",
    "contacts[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactGroupId` | string | yes | HappyFox contact group ID. |
| `contacts[]` | array<number> | yes | List of HappyFox contact IDs to remove from the group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Result details for the removal, including the contact ID and provider message. |
| `success` | boolean | Whether the contact was removed from the group successfully. |

## Native endpoint

Through the native HappyFox API, this operation is `POST /contact_group/:contact_group_id/delete_contacts/` (base URL `https://{{credentials.accountDomain}}/api/1.1/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-contacts-from-contact-group.md) for the provider-specific parameters and requirements.

