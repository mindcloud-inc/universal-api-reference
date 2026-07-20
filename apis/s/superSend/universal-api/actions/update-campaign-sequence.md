# SuperSend: Update Campaign Sequence

Updates a campaign sequence in SuperSend.

```
PUT https://connect.mindcloud.co/v1/universal/superSend/latest/actions/update-campaign-sequence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/update-campaign-sequence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superSend/latest/actions/update-campaign-sequence', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Resource ID (UUID) |
| `nodes[]` | array<object> | no |  |
| `nodes[].id` | string | no |  |
| `nodes[].type` | string | no |  |
| `nodes[].data` | object | no | Node-specific data (varies by node type). **For emailNode:** use `subject_a` and `body_a` (required). Do NOT use bare `subject` or `body` — these fields are rejected. For A/B testing also include `subject_b`/`body_b`, `subject_c`/`body_c`, or `subject_d`/`body_d`. Example emailNode data: ```json { "type": 1, "label": "Email Step 1", "subject_a": "Hello {{first_name}}", "body_a": "<p>Your email body</p>", "wait": 1, "wait_unit": "days" } ``` |
| `nodes[].position` | object | no |  |
| `nodes[].position.x` | number | no |  |
| `nodes[].position.y` | number | no |  |
| `nodes[].style` | object | no |  |
| `nodes[].style.width` | number | no |  |
| `nodes[].style.height` | number | no |  |
| `nodes[].style.minWidth` | number | no |  |
| `nodes[].style.minHeight` | number | no |  |
| `edges[]` | array<object> | no |  |
| `edges[].id` | string | no |  |
| `edges[].source` | string | no |  |
| `edges[].sourceHandle` | string | no |  |
| `edges[].target` | string | no |  |
| `edges[].type` | string | no | Allowed values: buttonedge. Default: buttonedge. |

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

Through the native SuperSend API, this operation is `PATCH /campaigns/{id}/sequence` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign-sequence.md) for the provider-specific parameters and requirements.

