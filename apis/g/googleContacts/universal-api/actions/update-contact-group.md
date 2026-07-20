# Google Contacts: Update Contact Group

Updates an existing contact group in Google Contacts.

```
PUT https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/update-contact-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/update-contact-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceName": "Ava Chen",
  "contactGroup.name": "Ava Chen",
  "contactGroup.etag": "string",
  "updateGroupFields": "name"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/update-contact-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceName": "Ava Chen",
    "contactGroup.name": "Ava Chen",
    "contactGroup.etag": "string",
    "updateGroupFields": "name"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceName` | string | yes | Contact group ID segment (for example, 4818b05f0a06bc27). |
| `contactGroup.name` | string | yes | Updated contact group name. |
| `contactGroup.etag` | string | yes | Current ETag of the contact group. |
| `updateGroupFields` | string | yes | Comma-separated field mask of ContactGroup fields to update. Default: `name`. |
| `readGroupFields` | string | no | Comma-separated fields to include in the updated group response. Default: `name,groupType,memberCount,metadata`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "formattedName": "Ava Chen",
      "groupType": "string",
      "metadata": {
        "updateTime": "2026-05-07T12:00:00.000Z"
      },
      "name": "Ava Chen",
      "resourceName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `formattedName` | string |  |
| `groupType` | string |  |
| `metadata.updateTime` | date |  |
| `name` | string |  |
| `resourceName` | string |  |

## Native endpoint

Through the native Google Contacts API, this operation is `PUT /v1/contactGroups/:resourceName` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-group.md) for the provider-specific parameters and requirements.

