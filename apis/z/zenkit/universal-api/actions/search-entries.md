# Zenkit: Search Entries

Searches for items in Zenkit.

```
GET https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/search-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/search-entries?connectionId=$CONNECTION_ID&excludeListEntryUUIDs%5B%5D=string&includeRelatedListElements=true&includeRelatedLists=true&includeRelatedWorkspaces=true&limit=1&preferredListIds%5B%5D=string&query=string&searchInArchive=true" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "excludeListEntryUUIDs[]": "string",
  "includeRelatedListElements": "true",
  "includeRelatedLists": "true",
  "includeRelatedWorkspaces": "true",
  "limit": "1",
  "preferredListIds[]": "string",
  "query": "string",
  "searchInArchive": "true"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/search-entries?${params}`, {
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
| `excludeListEntryUUIDs[]` | array<string> | yes | An array of list entry UUIDs to exclude from the search. |
| `includeRelatedListElements` | boolean | yes | If true, the result will include the list elements for the found entries. |
| `includeRelatedLists` | boolean | yes | If true, the result will include the lists where the entries were found. |
| `includeRelatedWorkspaces` | boolean | yes | If true, the result will include the workspaces where the entries were found. |
| `limit` | number | yes | The number of entries that will be returned. |
| `preferredListIds[]` | array<string> | yes | The IDs of the lists that should be searched first. |
| `query` | string | yes | The search string. |
| `searchInArchive` | boolean | yes | If true, deprecated entries will be searched. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "thereAreMoreResults": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `thereAreMoreResults` | boolean |  |

## Native endpoint

Through the native Zenkit API, this operation is `GET /entries/search` (base URL `https://zenkit.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-entries.md) for the provider-specific parameters and requirements.

