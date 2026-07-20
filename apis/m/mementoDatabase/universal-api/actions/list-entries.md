# Memento Database: List Entries

Retrieves entries from a library in Memento Database.

```
GET https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/list-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Memento Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/list-entries?connectionId=$CONNECTION_ID&libraryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "libraryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/list-entries?${params}`, {
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
| `libraryId` | string | yes | The ID of the library. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of entries to return. |
| `pageToken` | string | no | Page token returned by a previous list response. |
| `createdAfter` | string | no | Only return entries created after this ISO-8601 timestamp. |
| `updatedAfter` | string | no | Only return entries updated after this ISO-8601 timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entries": [
        {}
      ],
      "nextPageToken": "string",
      "revision": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entries` | array<object> |  |
| `nextPageToken` | string |  |
| `revision` | number |  |

## Native endpoint

Through the native Memento Database API, this operation is `GET /libraries/[:libraryId]/entries` (base URL `https://api.mementodatabase.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-entries.md) for the provider-specific parameters and requirements.

