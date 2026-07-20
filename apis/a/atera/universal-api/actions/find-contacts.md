# Atera: Find contacts

Finds contacts in Atera.

```
GET https://connect.mindcloud.co/v1/universal/atera/latest/actions/find-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atera `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atera/latest/actions/find-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atera/latest/actions/find-contacts?${params}`, {
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
| `searchOptions.email` | string | no | Filter contacts by email address. Example: `person@example.com`. |
| `searchOptions.phone` | string | no | Filter contacts by phone number. Example: `+1 415 555 0100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Archived": true,
      "CreatedOn": "string",
      "CustomerID": 1,
      "CustomerName": "Ava Chen",
      "Email": "ava@example.com",
      "EndUserID": 1,
      "Firstname": "Ava",
      "InIgnoreMode": true,
      "IsContactPerson": true,
      "JobTitle": "string",
      "LastModified": "string",
      "Lastname": "Chen",
      "Phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Archived` | boolean |  |
| `CreatedOn` | string |  |
| `CustomerID` | number |  |
| `CustomerName` | string |  |
| `Email` | string |  |
| `EndUserID` | number |  |
| `Firstname` | string |  |
| `InIgnoreMode` | boolean |  |
| `IsContactPerson` | boolean |  |
| `JobTitle` | string |  |
| `LastModified` | string |  |
| `Lastname` | string |  |
| `Phone` | string |  |

## Native endpoint

Through the native Atera API, this operation is `GET /api/v3/contacts` (base URL `https://app.atera.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/find-contacts.md) for the provider-specific parameters and requirements.

