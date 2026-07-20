# Memento Database: Update Entry

Updates an existing entry in a Memento Database library.

```
PUT https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/update-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Memento Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/update-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "libraryId": "string",
  "entryId": "string",
  "fields[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/update-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "libraryId": "string",
    "entryId": "string",
    "fields[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `libraryId` | string | yes | The ID of the library. |
| `entryId` | string | yes | The ID of the entry. |
| `fields[]` | array<object> | yes | An array of field objects to update. Example: [{"id":1,"value":"Updated"}] |

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

Through the native Memento Database API, this operation is `PATCH /libraries/[:libraryId]/entries/[:entryId]` (base URL `https://api.mementodatabase.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-entry.md) for the provider-specific parameters and requirements.

