# Exa: Create Webset Enrichment

Creates a new webset enrichment in Exa.

```
POST https://connect.mindcloud.co/v1/universal/exa/latest/actions/create-webset-enrichment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/exa/latest/actions/create-webset-enrichment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webset": "string",
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/exa/latest/actions/create-webset-enrichment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webset": "string",
    "description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webset` | string | yes | The id or externalId of the Webset |
| `description` | string | yes | Provide a description of the enrichment task you want to perform to each Webset Item. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | string | no | Format of the enrichment response. We automatically select the best format based on the description. If you want to explicitly specify the format, you can do so here. |
| `options[]` | array<object> | no | When the format is options, the different options for the enrichment agent to choose from. |
| `metadata` | object | no | Set of key-value pairs you want to associate with this object. |

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

Through the native Exa API, this operation is `POST /websets/v0/websets/:webset/enrichments` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webset-enrichment.md) for the provider-specific parameters and requirements.

