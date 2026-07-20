# Google Contacts: List Contact Groups

Retrieves contact groups from Google Contacts.

```
GET https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/list-contact-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/list-contact-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/list-contact-groups?${params}`, {
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
| `groupFields` | string | no | Comma-separated ContactGroup fields to include. Default: `name,groupType,memberCount,metadata`. |
| `pageSize` | number | no | Maximum number of groups to return. |
| `pageToken` | string | no | Token from a previous page. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `syncToken` | string | no | Sync token from prior full sync. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactGroups": [
        {
          "formattedName": "Ava Chen",
          "groupType": "string",
          "name": "Ava Chen",
          "resourceName": "Ava Chen"
        }
      ],
      "nextSyncToken": "string",
      "totalItems": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactGroups[].formattedName` | string |  |
| `contactGroups[].groupType` | string |  |
| `contactGroups[].name` | string |  |
| `contactGroups[].resourceName` | string |  |
| `nextSyncToken` | string |  |
| `totalItems` | number |  |

## Native endpoint

Through the native Google Contacts API, this operation is `GET /v1/contactGroups` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-groups.md) for the provider-specific parameters and requirements.

