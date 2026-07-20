# UseINBOX: Delete Single Contact From List

Deletes a contact from a list in UseINBOX.

```
DELETE https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/delete-single-contact-from-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UseINBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/delete-single-contact-from-list?connectionId=$CONNECTION_ID&id=string&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/delete-single-contact-from-list?${params}`, {
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
| `id` | string | yes | Contact list ID from INBOX. |
| `contactId` | string | yes | Contact ID to remove from the list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native UseINBOX API, this operation is `DELETE /inbox/v1/contactlists/:id/delete/:contact-id` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-single-contact-from-list.md) for the provider-specific parameters and requirements.

