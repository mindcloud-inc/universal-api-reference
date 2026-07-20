# mfr Field Service Management: Update Contact

Updates a contact in mfr Field Service Management.

```
PUT https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mfr Field Service Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "bodyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "bodyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `bodyId` | string | yes | Record ID in the request body. |
| `firstName` | string | no | Updated contact first name. |
| `lastName` | string | no | Updated contact last name. |
| `email` | string | no | Updated contact email address. |
| `jobTitle` | string | no | Updated job title. |
| `externalId` | string | no | Updated external identifier. |
| `mobilePhone` | string | no | Mobile phone number. |
| `telephone` | string | no | Telephone number. |
| `fax` | string | no | Fax number. |
| `note` | string | no | Contact note. |
| `companyId` | string | no | Associated company identifier. |
| `isUser` | boolean | no | Whether the contact is a user. |
| `gender` | string | no | Contact gender. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native mfr Field Service Management API returns.

## Native endpoint

Through the native mfr Field Service Management API, this operation is `PUT Contacts({{id}}L)` (base URL `https://portal.mobilefieldreport.com/odata`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

