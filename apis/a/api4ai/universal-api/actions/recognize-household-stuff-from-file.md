# api4ai: Recognize Household Stuff from File

Recognizes household items from an image file in api4ai.

```
GET https://connect.mindcloud.co/v1/universal/api4ai/latest/actions/recognize-household-stuff-from-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a api4ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/api4ai/latest/actions/recognize-household-stuff-from-file?connectionId=$CONNECTION_ID&image=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "image": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api4ai/latest/actions/recognize-household-stuff-from-file?${params}`, {
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
| `image` | file | yes | Household-item image file to analyze. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": {
        "entities": {
          "mapping": {}
        },
        "md5": "string",
        "name": "Ava Chen",
        "status": {
          "code": "string",
          "message": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> | Recognition results. |
| `results.entities.mapping` | object | Detected household items grouped by label. |
| `results.md5` | string | Processed image content hash. |
| `results.name` | string | Processed image name. |
| `results.status.code` | string | Processing status code. |
| `results.status.message` | string | Processing status message. |

## Native endpoint

Through the native api4ai API, this operation is `POST /household-stuff/v1/results` (base URL `https://api4ai.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/recognize-household-stuff-from-file.md) for the provider-specific parameters and requirements.

