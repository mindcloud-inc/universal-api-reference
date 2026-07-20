# Kylas CRM: Get Contact

Retrieves a contact from Kylas CRM by ID.

```
GET https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kylas CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/get-contact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/get-contact?${params}`, {
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
| `contactId` | string | no | The Kylas contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "createdBy": 1,
      "createdViaId": "string",
      "createdViaName": "Ava Chen",
      "createdViaType": "string",
      "dnd": true,
      "id": 1,
      "lastName": "Chen",
      "metaData": {},
      "ownerId": 1,
      "recordActions": {},
      "score": 1,
      "stakeholder": true,
      "updatedAt": "string",
      "updatedBy": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | UTC timestamp when the contact was created. |
| `createdBy` | number | User ID that created the contact. |
| `createdViaId` | string | Identifier for the source that created the contact. |
| `createdViaName` | string | Display name of the source that created the contact. |
| `createdViaType` | string | Type of the source that created the contact. |
| `dnd` | boolean | Whether the contact is marked do-not-disturb. |
| `id` | number | Kylas contact ID. |
| `lastName` | string | Contact last name. |
| `metaData` | object | Additional Kylas metadata for related display names. |
| `ownerId` | number | Owner user ID for the contact. |
| `recordActions` | object | Action permissions available on this contact record. |
| `score` | number | Kylas contact score. |
| `stakeholder` | boolean | Whether the contact is marked as a stakeholder. |
| `updatedAt` | string | UTC timestamp when the contact was last updated. |
| `updatedBy` | number | User ID that last updated the contact. |

## Native endpoint

Through the native Kylas CRM API, this operation is `GET /contacts/{contactId}` (base URL `https://api.kylas.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

