# Kylas CRM: Update Contact

Updates an existing contact in Kylas CRM.

```
PUT https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kylas CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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
      "stakeholder": true,
      "updatedAt": "string",
      "updatedBy": 1,
      "updatedViaId": "string",
      "updatedViaName": "Ava Chen",
      "updatedViaType": "string"
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
| `stakeholder` | boolean | Whether the contact is marked as a stakeholder. |
| `updatedAt` | string | UTC timestamp when the contact was last updated. |
| `updatedBy` | number | User ID that last updated the contact. |
| `updatedViaId` | string | Identifier for the source that last updated the contact. |
| `updatedViaName` | string | Display name of the source that last updated the contact. |
| `updatedViaType` | string | Type of the source that last updated the contact. |

## Native endpoint

Through the native Kylas CRM API, this operation is `PUT /contacts/{contactId}` (base URL `https://api.kylas.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

