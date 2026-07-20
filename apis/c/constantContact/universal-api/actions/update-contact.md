# Constant Contact: Update Contact

Updates a contact in Constant Contact.

```
PUT https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "updateSource": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "updateSource": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | Unique ID of the contact to update. |
| `updateSource` | string | yes | Source used for this contact update. |
| `emailAddress.address` | string | no | Updated primary email address. |
| `firstName` | string | no | Updated first name. |
| `lastName` | string | no | Updated last name. |
| `listMemberships[]` | array<string> | no | List IDs to set on update (array of strings). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createSource": "string",
      "emailAddress": {
        "address": "ava@example.com",
        "confirmStatus": "ava@example.com",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "optInDate": "2026-05-07T12:00:00.000Z",
        "optInSource": "ava@example.com",
        "permissionToSend": "ava@example.com",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "firstName": "Ava",
      "lastName": "Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updateSource": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | string |  |
| `createdAt` | date |  |
| `createSource` | string |  |
| `emailAddress` | object |  |
| `emailAddress.address` | string |  |
| `emailAddress.confirmStatus` | string |  |
| `emailAddress.createdAt` | date |  |
| `emailAddress.optInDate` | date |  |
| `emailAddress.optInSource` | string |  |
| `emailAddress.permissionToSend` | string |  |
| `emailAddress.updatedAt` | date |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `updatedAt` | date |  |
| `updateSource` | string |  |

## Native endpoint

Through the native Constant Contact API, this operation is `PUT /contacts/:contact_id` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

