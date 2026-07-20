# Strale: Get Transaction

Retrieves a transaction from Strale.

```
GET https://connect.mindcloud.co/v1/universal/strale/latest/actions/get-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strale/latest/actions/get-transaction?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strale/latest/actions/get-transaction?${params}`, {
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
| `id` | string | yes | Transaction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capabilitySlug": "string",
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dataJurisdiction": "string",
      "id": "string",
      "input": {
        "email": "ava@example.com"
      },
      "isFreeTier": true,
      "latencyMs": 1,
      "output": {
        "domain": "string",
        "email": "ava@example.com",
        "formatValid": true,
        "hasMxRecords": true,
        "isDisposable": true,
        "isFreeProvider": true,
        "isRoleAddress": true,
        "valid": true
      },
      "priceCents": 1,
      "provenance": {
        "fetchedAt": "2026-05-07T12:00:00.000Z",
        "source": "string"
      },
      "quality": {
        "qualityGrade": "string",
        "reliabilityGrade": "string",
        "sqs": 1,
        "sqsLabel": "string",
        "strategy": "string",
        "usable": true
      },
      "solutionSlug": "string",
      "status": "string",
      "transparencyMarker": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capabilitySlug` | string | Capability slug when the transaction is capability-based. |
| `completedAt` | date | Transaction completion timestamp. |
| `createdAt` | date | Transaction creation timestamp. |
| `dataJurisdiction` | string | Jurisdiction label for processed data. |
| `id` | string | Transaction identifier. |
| `input.email` | string | Submitted email input. |
| `isFreeTier` | boolean | Whether this run used a free-tier allowance. |
| `latencyMs` | number | Observed latency in milliseconds. |
| `output.domain` | string | Resolved email domain. |
| `output.email` | string | Validated email output. |
| `output.formatValid` | boolean | Whether the input format was valid. |
| `output.hasMxRecords` | boolean | Whether MX records were found for the domain. |
| `output.isDisposable` | boolean | Whether the email uses a disposable provider. |
| `output.isFreeProvider` | boolean | Whether the email uses a free email provider. |
| `output.isRoleAddress` | boolean | Whether the mailbox looks like a role address. |
| `output.valid` | boolean | Whether the email was considered valid. |
| `priceCents` | number | Transaction price in cents. |
| `provenance.fetchedAt` | date | When upstream data was fetched. |
| `provenance.source` | string | Primary provenance source. |
| `quality.qualityGrade` | string | Overall quality grade. |
| `quality.reliabilityGrade` | string | Overall reliability grade. |
| `quality.sqs` | number | Strale quality score for this transaction. |
| `quality.sqsLabel` | string | Human-readable transaction quality label. |
| `quality.strategy` | string | Execution strategy used for this result. |
| `quality.usable` | boolean | Whether the result is considered usable. |
| `solutionSlug` | string | Solution slug when the transaction is solution-based. |
| `status` | string | Transaction status. |
| `transparencyMarker` | string | Transparency marker for the execution path. |
| `type` | string | Transaction type. |

## Native endpoint

Through the native Strale API, this operation is `GET /v1/transactions/:id` (base URL `https://api.strale.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction.md) for the provider-specific parameters and requirements.

