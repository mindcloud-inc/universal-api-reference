# Formitize: Delete Contact

Deletes an existing contact from Formitize.

```
DELETE https://connect.mindcloud.co/v1/universal/formitize/latest/actions/delete-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formitize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/formitize/latest/actions/delete-contact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formitize/latest/actions/delete-contact?${params}`, {
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
| `contactId` | string | no | Formitize contact ID. |
| `id` | string | no | Formitize client ID for contact delete path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Formitize API, this operation is `DELETE /crm/client/:id/contact/:contactID` (base URL `https://service.formitize.com/api/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact.md) for the provider-specific parameters and requirements.

