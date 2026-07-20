# CATS: Search Contacts

Finds contacts in CATS by search query.

```
GET https://connect.mindcloud.co/v1/universal/cATS/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/search-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&query=MindCloud%20Stage3%20Contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "MindCloud Stage3 Contact"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cATS/latest/actions/search-contacts?${params}`, {
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
| `query` | string | yes | The string to search within contacts for. Example: `MindCloud Stage3 Contact`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "city": "string",
        "postalCode": "string",
        "state": "string",
        "street": "string"
      },
      "companyId": 1,
      "countryCode": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateModified": "2026-05-07T12:00:00.000Z",
      "emails": {
        "primary": "ava@example.com",
        "secondary": "ava@example.com"
      },
      "enteredById": 1,
      "firstName": "Ava",
      "hasLeftCompany": true,
      "id": 1,
      "isHot": true,
      "lastName": "Chen",
      "notes": "string",
      "ownerId": 1,
      "phones": {
        "cell": "string",
        "other": "string",
        "work": "string"
      },
      "reportsToId": 1,
      "statusId": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.city` | string |  |
| `address.postalCode` | string |  |
| `address.state` | string |  |
| `address.street` | string |  |
| `companyId` | number |  |
| `countryCode` | string |  |
| `dateCreated` | date |  |
| `dateModified` | date |  |
| `emails.primary` | string |  |
| `emails.secondary` | string |  |
| `enteredById` | number |  |
| `firstName` | string |  |
| `hasLeftCompany` | boolean |  |
| `id` | number |  |
| `isHot` | boolean |  |
| `lastName` | string |  |
| `notes` | string |  |
| `ownerId` | number |  |
| `phones.cell` | string |  |
| `phones.other` | string |  |
| `phones.work` | string |  |
| `reportsToId` | number |  |
| `statusId` | number |  |
| `title` | string |  |

## Native endpoint

Through the native CATS API, this operation is `GET /contacts/search` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

