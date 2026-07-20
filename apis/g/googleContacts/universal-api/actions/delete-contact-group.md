# Google Contacts: Delete Contact Group

Deletes an existing contact group from Google Contacts.

```
DELETE https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/delete-contact-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Contacts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/delete-contact-group?connectionId=$CONNECTION_ID&resourceName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/delete-contact-group?${params}`, {
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
| `resourceName` | string | yes | Contact group ID segment (for example, 4818b05f0a06bc27). |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deleteContacts` | boolean | no | If true, also delete member contacts when deleting the group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resourceName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resourceName` | string |  |

## Native endpoint

Through the native Google Contacts API, this operation is `DELETE /v1/contactGroups/:resourceName` (base URL `https://people.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-group.md) for the provider-specific parameters and requirements.

