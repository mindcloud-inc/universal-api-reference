# Explodely: Update Affiliate Referral Contract

Updates an affiliate referral contract in Explodely.

```
PUT https://connect.mindcloud.co/v1/universal/explodely/latest/actions/update-affiliate-referral-contract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Explodely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/explodely/latest/actions/update-affiliate-referral-contract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contractId": "12345",
  "affiliateCommission": "25"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/explodely/latest/actions/update-affiliate-referral-contract', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contractId": "12345",
    "affiliateCommission": "25"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contractId` | string | yes | The affiliate referral contract ID to edit. Example: `12345`. |
| `affiliateCommission` | string | yes | The updated partner share percentage, up to 80. Example: `25`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contract_edited": "string",
      "error": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contract_edited` | string |  |
| `error` | string |  |

## Native endpoint

Through the native Explodely API, this operation is `POST /aff` (base URL `https://explodely.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-affiliate-referral-contract.md) for the provider-specific parameters and requirements.

