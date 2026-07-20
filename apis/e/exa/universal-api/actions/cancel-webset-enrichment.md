# Exa: Cancel Webset Enrichment

Cancels a running webset enrichment in Exa.

```
PUT https://connect.mindcloud.co/v1/universal/exa/latest/actions/cancel-webset-enrichment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/exa/latest/actions/cancel-webset-enrichment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webset": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/exa/latest/actions/cancel-webset-enrichment', {
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
| `webset` | string | yes | The id or externalId of the Webset |
| `id` | string | yes | The id of the Enrichment |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "description": "string",
      "format": "string",
      "id": "string",
      "instructions": "string",
      "metadata": "string",
      "object": "string",
      "options": "string",
      "status": "string",
      "title": "string",
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
| `createdAt` | string |  |
| `description` | string |  |
| `format` | string |  |
| `id` | string |  |
| `instructions` | string |  |
| `metadata` | string |  |
| `object` | string |  |
| `options` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `websetId` | string |  |

## Native endpoint

Through the native Exa API, this operation is `POST /websets/v0/websets/:webset/enrichments/:id/cancel` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-webset-enrichment.md) for the provider-specific parameters and requirements.

