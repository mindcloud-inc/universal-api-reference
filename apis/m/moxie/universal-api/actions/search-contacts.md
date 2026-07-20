# Moxie: Search Contacts

Finds contacts in Moxie.

```
GET https://connect.mindcloud.co/v1/universal/moxie/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moxie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/search-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moxie/latest/actions/search-contacts?${params}`, {
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
| `query` | string | no | Optional search string that can match first, last, or email. Example: `Darryl Kelly`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "clientId": "string",
      "clientPortalUserId": 1,
      "defaultContact": true,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "importRecordId": "string",
      "invoiceContact": true,
      "lastName": "Chen",
      "mobile": "string",
      "notes": "string",
      "phone": "string",
      "portalAccess": true,
      "role": "string",
      "sampleData": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `clientId` | string |  |
| `clientPortalUserId` | number |  |
| `defaultContact` | boolean |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `importRecordId` | string |  |
| `invoiceContact` | boolean |  |
| `lastName` | string |  |
| `mobile` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `portalAccess` | boolean |  |
| `role` | string |  |
| `sampleData` | boolean |  |

## Native endpoint

Through the native Moxie API, this operation is `GET /action/contacts/search` (base URL `https://pod01.withmoxie.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

