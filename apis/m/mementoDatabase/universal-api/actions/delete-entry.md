# Memento Database: Delete Entry

Deletes an existing entry from a Memento Database library.

```
DELETE https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/delete-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Memento Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/delete-entry?connectionId=$CONNECTION_ID&libraryId=string&entryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "libraryId": "string",
  "entryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/delete-entry?${params}`, {
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
      "statusCode": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `statusCode` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Memento Database API, this operation is `DELETE /libraries/[:libraryId]/entries/[:entryId]` (base URL `https://api.mementodatabase.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-entry.md) for the provider-specific parameters and requirements.

