# mfr Field Service Management: List Companies

Retrieves companies from mfr Field Service Management.

```
GET https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mfr Field Service Management `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/list-companies?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native mfr Field Service Management API, this operation is `GET Companies` (base URL `https://portal.mobilefieldreport.com/odata`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

