# GoCardless: Cancel Mandate

Cancels an existing mandate in GoCardless.

```
PUT https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/cancel-mandate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/cancel-mandate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identity": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/cancel-mandate', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identity": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identity` | string | yes | ID of the mandate to cancel. |
| `data.metadata` | object | no | Optional metadata stored on the mandate cancellation event. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mandates": {
        "consentParameters": {},
        "consentType": {},
        "createdAt": "string",
        "fundsSettlement": "string",
        "id": "string",
        "links": {
          "creditor": "https://example.com",
          "customer": "https://example.com",
          "customerBankAccount": "https://example.com"
        },
        "nextPossibleChargeDate": {},
        "paymentsRequireApproval": true,
        "reference": "string",
        "scheme": "string",
        "status": "string",
        "verifiedAt": {}
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mandates.consentParameters` | object |  |
| `mandates.consentType` | object |  |
| `mandates.createdAt` | string |  |
| `mandates.fundsSettlement` | string |  |
| `mandates.id` | string |  |
| `mandates.links.creditor` | string |  |
| `mandates.links.customer` | string |  |
| `mandates.links.customerBankAccount` | string |  |
| `mandates.nextPossibleChargeDate` | object |  |
| `mandates.paymentsRequireApproval` | boolean |  |
| `mandates.reference` | string |  |
| `mandates.scheme` | string |  |
| `mandates.status` | string |  |
| `mandates.verifiedAt` | object |  |

## Native endpoint

Through the native GoCardless API, this operation is `POST /mandates/:identity/actions/cancel` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-mandate.md) for the provider-specific parameters and requirements.

