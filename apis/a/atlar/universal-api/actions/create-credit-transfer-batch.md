# Atlar: Create credit transfer batch

Creates a credit transfer batch in Atlar.

```
POST https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-credit-transfer-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-credit-transfer-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "treatment": "string",
  "payments[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlar/latest/actions/create-credit-transfer-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "treatment": "string",
    "payments[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `treatment` | string<string> | yes |  |
| `payments[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvalResults": {},
      "approvalSteps": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "creatorUserId": "string",
      "errors": [
        {}
      ],
      "etag": "string",
      "externalId": "string",
      "id": "string",
      "input": {},
      "inputContent": {},
      "inputDetails": {},
      "metadata": {},
      "organizationId": "string",
      "resultDetails": {},
      "results": {},
      "resultSummary": {},
      "status": "string",
      "treatment": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvalResults` | object |  |
| `approvalSteps` | array<object> |  |
| `created` | date |  |
| `creatorUserId` | string |  |
| `errors` | array<object> |  |
| `etag` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `input` | object |  |
| `inputContent` | object |  |
| `inputDetails` | object |  |
| `metadata` | object |  |
| `organizationId` | string |  |
| `resultDetails` | object |  |
| `results` | object |  |
| `resultSummary` | object |  |
| `status` | string |  |
| `treatment` | string |  |
| `updated` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Atlar API, this operation is `POST /payments/v2beta/credit-transfer-batches` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-credit-transfer-batch.md) for the provider-specific parameters and requirements.

