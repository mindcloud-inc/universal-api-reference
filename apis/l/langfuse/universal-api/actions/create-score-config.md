# Langfuse: Create Score Config

Creates a score config in Langfuse.

```
POST https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/create-score-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langfuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/create-score-config" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/create-score-config', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `categories` | string | no |  |
| `dataType` | string | no |  |
| `description` | string | no |  |
| `maxValue` | string | no |  |
| `minValue` | string | no |  |
| `name` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dataType": "string",
      "description": "string",
      "id": "string",
      "isArchived": true,
      "maxValue": 1,
      "minValue": 1,
      "name": "Ava Chen",
      "projectId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<object> |  |
| `createdAt` | date |  |
| `dataType` | string |  |
| `description` | string |  |
| `id` | string |  |
| `isArchived` | boolean |  |
| `maxValue` | number |  |
| `minValue` | number |  |
| `name` | string |  |
| `projectId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Langfuse API, this operation is `POST /score-configs` (base URL `https://cloud.langfuse.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-score-config.md) for the provider-specific parameters and requirements.

