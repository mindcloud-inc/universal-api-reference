# mfr Field Service Management: Find Contact by ID

Finds a contact in mfr Field Service Management by ID.

```
GET https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/find-contact-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mfr Field Service Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/find-contact-by-id?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/find-contact-by-id?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": 1,
      "customValues": [
        {}
      ],
      "dateModified": "string",
      "email": "ava@example.com",
      "externalId": "string",
      "fax": "string",
      "firstName": "Ava",
      "gender": "string",
      "groupId": "string",
      "id": 1,
      "isUser": true,
      "jobTitle": "string",
      "lastName": "Chen",
      "mobilePhone": "string",
      "note": "string",
      "telephone": "string",
      "userId": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | number |  |
| `customValues` | array<object> |  |
| `dateModified` | string |  |
| `email` | string |  |
| `externalId` | string |  |
| `fax` | string |  |
| `firstName` | string |  |
| `gender` | string |  |
| `groupId` | string |  |
| `id` | number |  |
| `isUser` | boolean |  |
| `jobTitle` | string |  |
| `lastName` | string |  |
| `mobilePhone` | string |  |
| `note` | string |  |
| `telephone` | string |  |
| `userId` | string |  |
| `version` | number |  |

## Native endpoint

Through the native mfr Field Service Management API, this operation is `GET Contacts?$filter=Id eq {{id}}L` (base URL `https://portal.mobilefieldreport.com/odata`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-contact-by-id.md) for the provider-specific parameters and requirements.

