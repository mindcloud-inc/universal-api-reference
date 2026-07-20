# Alto: Search Contacts

Finds contacts in Alto by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/search-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/search-contacts?${params}`, {
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
| `contactType` | string | no | Contact type filter. |
| `query` | string | yes | Search text for contacts. |
| `archived` | boolean | no | Whether to search archived contacts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "category": "string",
      "contactId": "string",
      "displayName": "Ava Chen",
      "id": "string",
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "registeredOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `category` | string |  |
| `contactId` | string |  |
| `displayName` | string |  |
| `id` | string |  |
| `modifiedDate` | date |  |
| `registeredOn` | date |  |

## Native endpoint

Through the native Alto API, this operation is `GET /contacts/search` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

