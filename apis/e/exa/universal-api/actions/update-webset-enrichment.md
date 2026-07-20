# Exa: Update Webset Enrichment

Updates an existing webset enrichment in Exa.

```
PUT https://connect.mindcloud.co/v1/universal/exa/latest/actions/update-webset-enrichment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/exa/latest/actions/update-webset-enrichment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webset": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/exa/latest/actions/update-webset-enrichment', {
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
| `webset` | string | yes |  |
| `id` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Provide a description of the enrichment task you want to perform to each Webset Item. |
| `format` | string | no | Format of the enrichment response. We automatically select the best format based on the description. If you want to explicitly specify the format, you can do so here. |
| `options[]` | array<object> | no | When the format is options, the different options for the enrichment agent to choose from. |
| `metadata` | object | no | Set of key-value pairs you want to associate with this object. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Exa API returns.

## Native endpoint

Through the native Exa API, this operation is `PATCH /websets/v0/websets/:webset/enrichments/:id` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webset-enrichment.md) for the provider-specific parameters and requirements.

