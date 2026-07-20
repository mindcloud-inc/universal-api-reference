# pixx.io: Get File

Retrieves a file from your pixx.io workspace.

```
GET https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pixx.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/get-file?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/get-file?${params}`, {
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
| `id` | number | yes | The pixx.io file ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file": {
        "fileName": "Ava Chen",
        "id": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file` | object |  |
| `file.fileName` | string |  |
| `file.id` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native pixx.io API, this operation is `GET /files/:id` (base URL `https://mindcloudpixx260413.px.media/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

