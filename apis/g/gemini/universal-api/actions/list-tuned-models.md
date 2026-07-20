# Gemini: List Tuned Models

Retrieves created tuned models from Gemini.

```
GET https://connect.mindcloud.co/v1/universal/gemini/latest/actions/list-tuned-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gemini `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gemini/latest/actions/list-tuned-models?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gemini/latest/actions/list-tuned-models?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | Optional filter expression for tuned models. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseModel": "string",
      "createTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "displayName": "Ava Chen",
      "name": "Ava Chen",
      "state": "string",
      "updateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseModel` | string | Base model used for tuning. |
| `createTime` | date | Tuned model creation timestamp. |
| `description` | string | Tuned model description. |
| `displayName` | string | Human-friendly tuned model name. |
| `name` | string | Tuned model resource name. |
| `state` | string | Current tuned model state. |
| `updateTime` | date | Last tuned model update timestamp. |

## Native endpoint

Through the native Gemini API, this operation is `GET v1beta/tunedModels` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tuned-models.md) for the provider-specific parameters and requirements.

