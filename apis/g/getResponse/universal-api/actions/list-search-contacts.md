# GetResponse: List Search Contacts

Retrieves saved search contact lists from GetResponse.

```
GET https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/list-search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetResponse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/list-search-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/list-search-contacts?${params}`, {
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
| `name` | string | no | Filter search contacts by name |
| `createdOnFrom` | string | no | Return search contacts created on or after this date |
| `createdOnTo` | string | no | Return search contacts created on or before this date |
| `sortName` | string | no | Sort search contacts by name |
| `sortCreatedOn` | string | no | Sort search contacts by creation date |
| `fields` | string | no | Comma-separated list of fields to return |

## Response

```json
{
  "success": true,
  "data": [
    {
      "href": "string",
      "name": "Ava Chen",
      "searchContactId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `href` | string |  |
| `name` | string |  |
| `searchContactId` | string |  |

## Native endpoint

Through the native GetResponse API, this operation is `GET /search-contacts` (base URL `https://api.getresponse.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-search-contacts.md) for the provider-specific parameters and requirements.

