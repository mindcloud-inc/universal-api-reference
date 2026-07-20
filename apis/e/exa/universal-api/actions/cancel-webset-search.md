# Exa: Cancel Webset Search

Cancels a running webset search in Exa.

```
PUT https://connect.mindcloud.co/v1/universal/exa/latest/actions/cancel-webset-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/exa/latest/actions/cancel-webset-search" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webset": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/exa/latest/actions/cancel-webset-search', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webset": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webset` | string | yes | The id of the Webset |
| `id` | string | yes | The id of the Search |

## Response

```json
{
  "success": true,
  "data": [
    {
      "behavior": "string",
      "canceledAt": "string",
      "canceledReason": "string",
      "count": "string",
      "createdAt": "string",
      "criteria": "string",
      "entity": {
        "description": "string",
        "type": "string"
      },
      "exclude": "string",
      "id": "string",
      "metadata": "string",
      "object": "string",
      "progress": {
        "analyzed": "string",
        "completion": "string",
        "found": "string",
        "timeLeft": "string"
      },
      "query": "string",
      "recall": {},
      "scope": "string",
      "status": "string",
      "updatedAt": "string",
      "websetId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `behavior` | string |  |
| `canceledAt` | string |  |
| `canceledReason` | string |  |
| `count` | string |  |
| `createdAt` | string |  |
| `criteria` | string |  |
| `entity` | object |  |
| `entity.description` | string |  |
| `entity.type` | string |  |
| `exclude` | string |  |
| `id` | string |  |
| `metadata` | string |  |
| `object` | string |  |
| `progress` | object |  |
| `progress.analyzed` | string |  |
| `progress.completion` | string |  |
| `progress.found` | string |  |
| `progress.timeLeft` | string |  |
| `query` | string |  |
| `recall` | object |  |
| `scope` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |
| `websetId` | string |  |

## Native endpoint

Through the native Exa API, this operation is `POST /websets/v0/websets/:webset/searches/:id/cancel` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-webset-search.md) for the provider-specific parameters and requirements.

