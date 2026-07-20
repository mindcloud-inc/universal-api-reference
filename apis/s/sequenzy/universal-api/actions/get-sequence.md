# Sequenzy: Get Sequence

Retrieves sequence metadata and steps from Sequenzy.

```
GET https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/get-sequence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sequenzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/get-sequence?connectionId=$CONNECTION_ID&sequenceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sequenceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/get-sequence?${params}`, {
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
| `sequenceId` | string | yes | Sequence ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sequence": {
        "createdAt": "string",
        "emailCount": 1,
        "enrichedCount": 1,
        "enrichmentStatus": "string",
        "id": "string",
        "name": "Ava Chen",
        "nodes": {
          "automationId": "string",
          "config": {},
          "createdAt": "string",
          "id": "string",
          "nodeType": "string",
          "position": {},
          "updatedAt": "string"
        },
        "status": "string",
        "trigger": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sequence.createdAt` | string |  |
| `sequence.emailCount` | number |  |
| `sequence.enrichedCount` | number |  |
| `sequence.enrichmentStatus` | string |  |
| `sequence.id` | string |  |
| `sequence.name` | string |  |
| `sequence.nodes` | array<object> |  |
| `sequence.nodes.automationId` | string |  |
| `sequence.nodes.config` | object |  |
| `sequence.nodes.createdAt` | string |  |
| `sequence.nodes.id` | string |  |
| `sequence.nodes.nodeType` | string |  |
| `sequence.nodes.position` | object |  |
| `sequence.nodes.updatedAt` | string |  |
| `sequence.status` | string |  |
| `sequence.trigger` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Sequenzy API, this operation is `GET /sequences/:sequenceId` (base URL `https://api.sequenzy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sequence.md) for the provider-specific parameters and requirements.

