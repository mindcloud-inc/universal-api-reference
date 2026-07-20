# GoCardless: Create Mandate

Creates a new mandate in GoCardless.

```
POST https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/create-mandate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/create-mandate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "links.customerBankAccount": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/create-mandate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "links.customerBankAccount": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scheme` | string | no |  |
| `links` | object | no |  |
| `links.customerBankAccount` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authorisationSource` | list | no | One of: `0`, `1`, `2`. |
| `payerIpAddress` | string | no |  |
| `reference` | string | no |  |
| `metadata` | object | no |  |
| `links.creditor` | string | no |  |

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
        "nextPossibleChargeDate": "string",
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
| `mandates.nextPossibleChargeDate` | string |  |
| `mandates.paymentsRequireApproval` | boolean |  |
| `mandates.reference` | string |  |
| `mandates.scheme` | string |  |
| `mandates.status` | string |  |
| `mandates.verifiedAt` | object |  |

## Native endpoint

Through the native GoCardless API, this operation is `POST /mandates` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mandate.md) for the provider-specific parameters and requirements.

