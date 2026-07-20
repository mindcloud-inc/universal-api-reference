# Google Contacts: Get Contact Group

Retrieves a contact group from Google Contacts.

```
GET https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/get-contact-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/get-contact-group?connectionId=$CONNECTION_ID&resourceName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/get-contact-group?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceName` | string | yes | Contact group ID segment (for example, myContacts or 4818b05f0a06bc27). |
| `groupFields` | string | no | Comma-separated ContactGroup fields to include. Default: `name,groupType,memberCount,metadata`. |
| `maxMembers` | number | no | Maximum number of member resource names to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "formattedName": "Ava Chen",
      "groupType": "string",
      "memberCount": 1,
      "memberResourceNames": [
        "Ava Chen"
      ],
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
| `memberCount` | number |  |
| `memberResourceNames[]` | string |  |
| `metadata.updateTime` | date |  |
| `name` | string |  |
| `resourceName` | string |  |

## Native endpoint

Through the native Google Contacts API, this operation is `GET /v1/contactGroups/:resourceName` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-group.md) for the provider-specific parameters and requirements.

