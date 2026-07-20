# FuseDesk: Search Contacts

Finds contacts in FuseDesk by matching search text.

```
GET https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FuseDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/search-contacts?connectionId=$CONNECTION_ID&search=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "search": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/search-contacts?${params}`, {
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
| `search` | string | yes | Search text for matching contacts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "crmId": 1,
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateUpdated": "2026-05-07T12:00:00.000Z",
      "emailAddress": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "phone1": "string",
      "timeZone": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `crmId` | number |  |
| `dateCreated` | date |  |
| `dateUpdated` | date |  |
| `emailAddress` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `phone1` | string |  |
| `timeZone` | string |  |
| `website` | string |  |

## Native endpoint

Through the native FuseDesk API, this operation is `GET /api/v2/contacts` (base URL `https://{{credentials.appName}}.fusedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

