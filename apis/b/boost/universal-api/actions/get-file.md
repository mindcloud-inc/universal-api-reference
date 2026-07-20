# Boost: Get File

Retrieves a file record from Boost by ID.

```
GET https://connect.mindcloud.co/v1/universal/boost/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Boost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boost/latest/actions/get-file?connectionId=$CONNECTION_ID&fileId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boost/latest/actions/get-file?${params}`, {
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
| `fileId` | number | yes | Boost.space file ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "mime": "string",
      "name": "Ava Chen",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Creation timestamp. |
| `id` | number | File ID. |
| `mime` | string | MIME type. |
| `name` | string | File name. |
| `size` | number | File size. |

## Native endpoint

Through the native Boost API, this operation is `GET /file/{fileId}` (base URL `https://{{credentials.systemKey}}.boost.space/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

