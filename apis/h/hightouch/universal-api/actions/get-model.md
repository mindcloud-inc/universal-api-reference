# Hightouch: Get Model

Retrieves a model from Hightouch.

```
GET https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/get-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/get-model?connectionId=$CONNECTION_ID&modelId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/get-model?${params}`, {
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
| `modelId` | number | yes | The model ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "queryType": "string",
      "slug": "string",
      "sourceId": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `description` | string | Model description. |
| `id` | number | Model ID. |
| `name` | string | Model name. |
| `queryType` | string | Model query type. |
| `slug` | string | Model slug. |
| `sourceId` | number | Connected source ID. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native Hightouch API, this operation is `GET /models/{modelId}` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model.md) for the provider-specific parameters and requirements.

