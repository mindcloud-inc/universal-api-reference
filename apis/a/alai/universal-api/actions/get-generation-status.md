# Alai: Get Generation Status

Retrieves async operation status from Alai.

```
GET https://connect.mindcloud.co/v1/universal/alai/latest/actions/get-generation-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alai/latest/actions/get-generation-status?connectionId=$CONNECTION_ID&generationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "generationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alai/latest/actions/get-generation-status?${params}`, {
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
| `generationId` | string | yes | Generation identifier returned by an async create or export call. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "error": {},
      "formats": {
        "ppt": {
          "error": {},
          "status": "string",
          "url": "https://example.com"
        }
      },
      "generationId": "string",
      "generationType": "string",
      "presentationId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | date |  |
| `createdAt` | date |  |
| `error` | object |  |
| `formats.ppt.error` | object |  |
| `formats.ppt.status` | string |  |
| `formats.ppt.url` | string |  |
| `generationId` | string |  |
| `generationType` | string |  |
| `presentationId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Alai API, this operation is `GET /generations/:generation_id` (base URL `https://slides-api.getalai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-generation-status.md) for the provider-specific parameters and requirements.

