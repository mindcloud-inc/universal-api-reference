# SuperSend: Get Campaign Sequence

Retrieves a campaign sequence from SuperSend.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-campaign-sequence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-campaign-sequence?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-campaign-sequence?${params}`, {
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
| `id` | string | yes | Resource ID (UUID) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign_id": "string",
      "edges": [
        {
          "id": "string",
          "source": "string",
          "sourceHandle": "string",
          "target": "string",
          "type": "string"
        }
      ],
      "nodes": [
        {
          "data": {},
          "id": "string",
          "position": {
            "x": 1,
            "y": 1
          },
          "style": {
            "height": 1,
            "minHeight": 1,
            "minWidth": 1,
            "width": 1
          },
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign_id` | string |  |
| `edges[].id` | string |  |
| `edges[].source` | string |  |
| `edges[].sourceHandle` | string |  |
| `edges[].target` | string |  |
| `edges[].type` | string |  |
| `nodes[].data` | object |  |
| `nodes[].id` | string |  |
| `nodes[].position.x` | number |  |
| `nodes[].position.y` | number |  |
| `nodes[].style.height` | number |  |
| `nodes[].style.minHeight` | number |  |
| `nodes[].style.minWidth` | number |  |
| `nodes[].style.width` | number |  |
| `nodes[].type` | string |  |

## Native endpoint

Through the native SuperSend API, this operation is `GET /campaigns/{id}/sequence` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-sequence.md) for the provider-specific parameters and requirements.

