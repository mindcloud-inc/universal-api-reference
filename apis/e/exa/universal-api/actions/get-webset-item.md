# Exa: Get Webset Item

Retrieves a webset item from Exa.

```
GET https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-webset-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-webset-item?connectionId=$CONNECTION_ID&webset=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webset": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-webset-item?${params}`, {
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
| `webset` | string | yes | The id or externalId of the Webset |
| `id` | string | yes | The id of the Webset item |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "enrichments": {
        "enrichmentId": "string",
        "format": "string",
        "object": "string",
        "reasoning": "string",
        "references": "string",
        "result": "string",
        "status": "string"
      },
      "evaluations": "string",
      "id": "string",
      "object": "string",
      "properties": {},
      "source": "string",
      "sourceId": "string",
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
| `enrichments` | array<object> |  |
| `enrichments.enrichmentId` | string |  |
| `enrichments.format` | string |  |
| `enrichments.object` | string |  |
| `enrichments.reasoning` | string |  |
| `enrichments.references` | string |  |
| `enrichments.result` | string |  |
| `enrichments.status` | string |  |
| `evaluations` | string |  |
| `id` | string |  |
| `object` | string |  |
| `properties` | object |  |
| `source` | string |  |
| `sourceId` | string |  |
| `updatedAt` | string |  |
| `websetId` | string |  |

## Native endpoint

Through the native Exa API, this operation is `GET /websets/v0/websets/:webset/items/:id` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webset-item.md) for the provider-specific parameters and requirements.

