# Timizer: Delete Client Contact

Deletes an existing client contact from Timizer.

```
DELETE https://connect.mindcloud.co/v1/universal/timizer/latest/actions/delete-client-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/timizer/latest/actions/delete-client-contact?connectionId=$CONNECTION_ID&contactId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timizer/latest/actions/delete-client-contact?${params}`, {
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
| `contactId` | number | yes | ID of the contact. |
| `id` | number | yes | ID of the client. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Timizer API, this operation is `DELETE /app/clients/:id/contacts/:contactId` (base URL `https://api.timizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-client-contact.md) for the provider-specific parameters and requirements.

