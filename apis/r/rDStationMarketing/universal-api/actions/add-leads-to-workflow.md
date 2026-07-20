# RD Station Marketing: Add Leads to Workflow



```
POST https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/add-leads-to-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/add-leads-to-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "leads[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/add-leads-to-workflow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "leads[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Workflow ID in path. |
| `leads[]` | array<string> | yes | Lista de leads para enviar ao workflow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "leadsAdded": [
        [
          "string"
        ]
      ],
      "leadsNotFound": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `leadsAdded[]` | array<string> |  |
| `leadsNotFound[]` | array<string> |  |

## Native endpoint

Through the native RD Station Marketing API, this operation is `POST /platform/workflows/:id/leads` (base URL `https://api.rd.services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-leads-to-workflow.md) for the provider-specific parameters and requirements.

