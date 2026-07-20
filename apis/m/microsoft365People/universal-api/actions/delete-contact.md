# Microsoft 365 People: Delete Contact

Deletes an existing contact from Microsoft 365 People.

```
DELETE https://connect.mindcloud.co/v1/universal/microsoft365People/latest/actions/delete-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/microsoft365People/latest/actions/delete-contact?connectionId=$CONNECTION_ID&contactId=AAMkAG..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "AAMkAG..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365People/latest/actions/delete-contact?${params}`, {
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
| `contactId` | string | yes | The ID of the Outlook contact to delete. Example: `AAMkAG...`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft 365 People API returns.

## Native endpoint

Through the native Microsoft 365 People API, this operation is `DELETE /v1.0/me/contacts/{{contactId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact.md) for the provider-specific parameters and requirements.

