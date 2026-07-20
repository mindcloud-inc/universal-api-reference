# mfr Field Service Management: Create Company

Creates a company in mfr Field Service Management.

```
POST https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mfr Field Service Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Company name. |
| `externalId` | string | no | External identifier for the company. |
| `isPhysicalPerson` | boolean | no | Whether the company is a physical person. |
| `location` | object | no | Company location object. |
| `note` | string | no | Company note. |
| `supportTelephone` | string | no | Support telephone number. |
| `supportFax` | string | no | Support fax number. |
| `supportMail` | string | no | Support email address. |
| `isSupplier` | boolean | no | Whether the company is a supplier. |
| `mainContactId` | string | no | Main contact ID for the company. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingAddress": {},
      "customValues": [
        {}
      ],
      "dateModified": "2026-05-07T12:00:00.000Z",
      "dateOfCreation": "string",
      "externalId": "string",
      "id": 1,
      "isEmailInvoicingActive": true,
      "isOwner": true,
      "isPhysicalPerson": true,
      "isSupplier": true,
      "location": {},
      "mainContactId": "string",
      "mappingId": "string",
      "name": "Ava Chen",
      "note": "string",
      "quickSearch": "string",
      "supportFax": "string",
      "supportMail": "string",
      "supportTelephone": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingAddress` | object |  |
| `customValues` | array<object> |  |
| `dateModified` | date |  |
| `dateOfCreation` | string |  |
| `externalId` | string |  |
| `id` | number |  |
| `isEmailInvoicingActive` | boolean |  |
| `isOwner` | boolean |  |
| `isPhysicalPerson` | boolean |  |
| `isSupplier` | boolean |  |
| `location` | object |  |
| `mainContactId` | string |  |
| `mappingId` | string |  |
| `name` | string |  |
| `note` | string |  |
| `quickSearch` | string |  |
| `supportFax` | string |  |
| `supportMail` | string |  |
| `supportTelephone` | string |  |
| `version` | number |  |

## Native endpoint

Through the native mfr Field Service Management API, this operation is `POST Companies` (base URL `https://portal.mobilefieldreport.com/odata`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

