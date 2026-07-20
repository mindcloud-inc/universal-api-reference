# Contacts+: Delete Contact

Deletes an existing contact from Contacts+.

```
DELETE https://connect.mindcloud.co/v1/universal/contacts/latest/actions/delete-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Contacts+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/contacts/latest/actions/delete-contact?connectionId=$CONNECTION_ID&contactId=string&etag=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string",
  "etag": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contacts/latest/actions/delete-contact?${params}`, {
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
| `contactId` | string | yes | The contact ID to delete. |
| `etag` | string | yes | The current contact ETag. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | no | Delete the contact from this team instead of personal contacts. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Contacts+ API returns.

## Native endpoint

Through the native Contacts+ API, this operation is `POST /api/v1/contacts.delete` (base URL `https://api.contactsplus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact.md) for the provider-specific parameters and requirements.

