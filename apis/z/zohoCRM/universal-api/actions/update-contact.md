# Zoho CRM: Update Contact

Updates an existing contact in Zoho CRM.

```
PUT https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[]": [
    {}
  ],
  "data[].id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[]": [{}],
    "data[].id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[]` | array<object> | yes | Contact records to update. |
| `data[].id` | string | yes |  |
| `data[].lastName` | string | no | Example: `Wizard Contact 20260311 1 Updated`. |
| `data[].email` | string | no | Example: `wizard.contact.20260311.1.updated@example.com`. |
| `data[].a2zContactID` | string | no |  |
| `data[].company` | string | no |  |
| `data[].firstName` | string | no |  |
| `data[].middleName` | string | no |  |
| `data[].title` | string | no |  |
| `data[].website` | string | no |  |
| `data[].mailingCity` | string | no |  |
| `data[].mailingCountry` | string | no |  |
| `data[].mailingZip` | string | no |  |
| `data[].mailingState` | string | no |  |
| `data[].mailingStreet` | string | no |  |
| `data[].mailingStreet2` | string | no |  |
| `data[].accountName` | string | no |  |
| `data[].contactType` | string | no |  |
| `data[].tpe27ConfirmedExhibitor` | boolean | no |  |
| `data[].confirmedExhibitor` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "details": {
        "createdBy": {
          "id": "string",
          "name": "Ava Chen"
        },
        "createdTime": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "modifiedBy": {
          "id": "string",
          "name": "Ava Chen"
        },
        "modifiedTime": "2026-05-07T12:00:00.000Z"
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `details.createdBy.id` | string |  |
| `details.createdBy.name` | string |  |
| `details.createdTime` | date |  |
| `details.id` | string |  |
| `details.modifiedBy.id` | string |  |
| `details.modifiedBy.name` | string |  |
| `details.modifiedTime` | date |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho CRM API, this operation is `PUT /Contacts` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

