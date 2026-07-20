# Evalandgo: Download Question Upload Files

Retrieves uploaded files for a question from Evalandgo.

```
GET https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/download-question-upload-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evalandgo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/download-question-upload-files?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/download-question-upload-files?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Evalandgo API, this operation is `GET /api/v3/questions/upload/:id/download` (base URL `https://app.evalandgo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-question-upload-files.md) for the provider-specific parameters and requirements.

