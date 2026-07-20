# Memento Database: Get Entry

Retrieves an entry from a Memento Database library.

```
GET https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/get-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Memento Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/get-entry?connectionId=$CONNECTION_ID&libraryId=string&entryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "libraryId": "string",
  "entryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/get-entry?${params}`, {
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
| `entryId` | string | yes | The ID of the entry. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "createdTime": "string",
      "fields": [
        {}
      ],
      "id": "string",
      "modifiedTime": "string",
      "revision": 1,
      "size": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `createdTime` | string |  |
| `fields` | array<object> |  |
| `id` | string |  |
| `modifiedTime` | string |  |
| `revision` | number |  |
| `size` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Memento Database API, this operation is `GET /libraries/[:libraryId]/entries/[:entryId]` (base URL `https://api.mementodatabase.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-entry.md) for the provider-specific parameters and requirements.

