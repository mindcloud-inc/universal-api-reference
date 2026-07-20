# Atlar: Get credit transfer batch

Retrieves a credit transfer batch from Atlar.

```
GET https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-credit-transfer-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-credit-transfer-batch?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-credit-transfer-batch?${params}`, {
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
| `id` | string<string> | yes |  |

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

Through the native Atlar API, this operation is `GET /payments/v2beta/credit-transfer-batches/{id}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credit-transfer-batch.md) for the provider-specific parameters and requirements.

