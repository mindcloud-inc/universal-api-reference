# Strale: Verify Transaction Integrity

Verifies a transaction integrity trail in Strale.

```
GET https://connect.mindcloud.co/v1/universal/strale/latest/actions/verify-transaction-integrity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strale/latest/actions/verify-transaction-integrity?connectionId=$CONNECTION_ID&transactionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strale/latest/actions/verify-transaction-integrity?${params}`, {
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
| `depth` | number | no | Maximum chain depth to verify. |
| `transactionId` | string | yes | Transaction ID to verify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chain": {
        "brokenLinks": 1,
        "chainEndDate": "2026-05-07T12:00:00.000Z",
        "chainStartDate": "2026-05-07T12:00:00.000Z",
        "length": 1,
        "maxDepth": 1,
        "reachesGenesis": true,
        "truncated": true,
        "truncatedReason": "string",
        "verifiedLinks": 1
      },
      "hashValid": true,
      "methodologyUrl": "https://example.com",
      "transactionId": "string",
      "transactionMetadata": {
        "capabilitySlug": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "dataJurisdiction": "string",
        "status": "string",
        "transparencyMarker": "string"
      },
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chain.brokenLinks` | number | Number of broken chain links. |
| `chain.chainEndDate` | date | Latest verified chain date. |
| `chain.chainStartDate` | date | Earliest verified chain date. |
| `chain.length` | number | Number of chain records inspected. |
| `chain.maxDepth` | number | Maximum verification depth requested. |
| `chain.reachesGenesis` | boolean | Whether the chain reaches genesis. |
| `chain.truncated` | boolean | Whether the verification chain was truncated. |
| `chain.truncatedReason` | string | Reason the chain was truncated. |
| `chain.verifiedLinks` | number | Number of verified chain links. |
| `hashValid` | boolean | Whether the transaction hash matched the chain. |
| `methodologyUrl` | string | Verification methodology reference URL. |
| `transactionId` | string | Transaction identifier. |
| `transactionMetadata.capabilitySlug` | string | Capability slug tied to the transaction. |
| `transactionMetadata.createdAt` | date | Transaction creation timestamp. |
| `transactionMetadata.dataJurisdiction` | string | Jurisdiction label for processed data. |
| `transactionMetadata.status` | string | Transaction status. |
| `transactionMetadata.transparencyMarker` | string | Transparency marker on the transaction. |
| `verified` | boolean | Whether the integrity check passed. |

## Native endpoint

Through the native Strale API, this operation is `GET /v1/verify/:transactionId` (base URL `https://api.strale.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-transaction-integrity.md) for the provider-specific parameters and requirements.

