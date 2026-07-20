# Google Contacts: Modify Contact Group Members

Updates contact group membership in Google Contacts.

```
PUT https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/modify-contact-group-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/modify-contact-group-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/modify-contact-group-members', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceName` | string | yes | Contact group ID segment (for example, 4818b05f0a06bc27). |
| `resourceNamesToAdd[]` | array<string> | no | Person resource names to add to the group. |
| `resourceNamesToRemove[]` | array<string> | no | Person resource names to remove from the group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canNotRemoveLastContactGroupResourceNames": [
        "Ava Chen"
      ],
      "notFoundResourceNames": [
        "Ava Chen"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canNotRemoveLastContactGroupResourceNames[]` | string |  |
| `notFoundResourceNames[]` | string |  |

## Native endpoint

Through the native Google Contacts API, this operation is `POST /v1/contactGroups/:resourceName/members\:modify` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-contact-group-members.md) for the provider-specific parameters and requirements.

