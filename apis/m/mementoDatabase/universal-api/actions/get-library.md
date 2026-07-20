# Memento Database: Get Library

Retrieves a library from Memento Database.

```
GET https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/get-library
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Memento Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/get-library?connectionId=$CONNECTION_ID&libraryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "libraryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/get-library?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "string",
      "fields": [
        {}
      ],
      "id": "string",
      "modifiedTime": "string",
      "name": "Ava Chen",
      "owner": "string",
      "revision": 1,
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | string |  |
| `fields` | array<object> |  |
| `id` | string |  |
| `modifiedTime` | string |  |
| `name` | string |  |
| `owner` | string |  |
| `revision` | number |  |
| `size` | number |  |

## Native endpoint

Through the native Memento Database API, this operation is `GET /libraries/[:libraryId]` (base URL `https://api.mementodatabase.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-library.md) for the provider-specific parameters and requirements.

