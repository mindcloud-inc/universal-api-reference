# Google Contacts: Create Contact Group

Creates a new contact group in Google Contacts.

```
POST https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/create-contact-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/create-contact-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactGroup.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/create-contact-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactGroup.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactGroup.name` | string | yes | Display name for the new contact group. |
| `readGroupFields` | string | no | Comma-separated fields to include in the created group response. Default: `name,groupType,memberCount,metadata`. |

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

Through the native Google Contacts API, this operation is `POST /v1/contactGroups` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-group.md) for the provider-specific parameters and requirements.

