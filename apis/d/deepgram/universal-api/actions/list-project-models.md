# Deepgram: List Project Models

Retrieves project models from Deepgram.

```
GET https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-project-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepgram `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-project-models?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-project-models?${params}`, {
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
| `projectId` | string | yes | The Deepgram project identifier to inspect. |
| `includeOutdated` | boolean | no | Whether to include non-latest project model versions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "architecture": "string",
      "batch": true,
      "canonicalName": "Ava Chen",
      "formattedOutput": true,
      "languages": [
        "string"
      ],
      "name": "Ava Chen",
      "streaming": true,
      "uuid": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `architecture` | string |  |
| `batch` | boolean |  |
| `canonicalName` | string |  |
| `formattedOutput` | boolean |  |
| `languages` | array<string> |  |
| `name` | string |  |
| `streaming` | boolean |  |
| `uuid` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Deepgram API, this operation is `GET /v1/projects/:project_id/models` (base URL `https://api.deepgram.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-models.md) for the provider-specific parameters and requirements.

