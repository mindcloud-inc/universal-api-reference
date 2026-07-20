# Escrow.com: Get Transaction by Reference

Retrieves a transaction from Escrow.com by reference.

```
GET https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-transaction-by-reference
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Escrow.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-transaction-by-reference?connectionId=$CONNECTION_ID&reference=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reference": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-transaction-by-reference?${params}`, {
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
| `reference` | string | yes | The external reference for the transaction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "closeDate": "2026-05-07T12:00:00.000Z",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "description": "string",
      "id": 1,
      "isCancelled": true,
      "items": [
        {}
      ],
      "parties": [
        {}
      ],
      "partnerId": 1,
      "reference": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closeDate` | date | Transaction close timestamp when available. |
| `creationDate` | date | Transaction creation timestamp. |
| `currency` | string | Transaction currency code. |
| `description` | string | Transaction description. |
| `id` | number | Escrow.com transaction ID. |
| `isCancelled` | boolean | Whether the transaction has been cancelled. |
| `items` | array<object> | Items or milestones included in the transaction. |
| `parties` | array<object> | Parties participating in the transaction. |
| `partnerId` | number | Partner identifier associated with the transaction. |
| `reference` | string | External reference supplied for the transaction. |

## Native endpoint

Through the native Escrow.com API, this operation is `GET /transaction/reference/:reference` (base URL `https://api.escrow-sandbox.com/2017-09-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction-by-reference.md) for the provider-specific parameters and requirements.

