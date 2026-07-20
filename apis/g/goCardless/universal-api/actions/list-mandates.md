# GoCardless: List Mandates

Finds mandates in your GoCardless account.

```
GET https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-mandates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-mandates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-mandates?${params}`, {
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
| `createdAt` | object | no | Created-at range filters for mandate records. |
| `createdAt.gt` | date | no |  |
| `createdAt.gte` | date | no |  |
| `createdAt.lt` | date | no |  |
| `createdAt.lte` | date | no |  |
| `creditor` | string | no |  |
| `customer` | string | no |  |
| `customerBankAccount` | string | no |  |
| `mandateType` | string | no |  |
| `reference` | string | no |  |
| `scheme` | string | no |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mandates": [
        {
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
      ],
      "meta": {
        "cursors": {
          "after": {},
          "before": {}
        },
        "limit": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mandates[].consentParameters` | object |  |
| `mandates[].consentType` | object |  |
| `mandates[].createdAt` | string |  |
| `mandates[].fundsSettlement` | string |  |
| `mandates[].id` | string |  |
| `mandates[].links.creditor` | string |  |
| `mandates[].links.customer` | string |  |
| `mandates[].links.customerBankAccount` | string |  |
| `mandates[].nextPossibleChargeDate` | string |  |
| `mandates[].paymentsRequireApproval` | boolean |  |
| `mandates[].reference` | string |  |
| `mandates[].scheme` | string |  |
| `mandates[].status` | string |  |
| `mandates[].verifiedAt` | object |  |
| `meta.cursors.after` | object |  |
| `meta.cursors.before` | object |  |
| `meta.limit` | number |  |

## Native endpoint

Through the native GoCardless API, this operation is `GET /mandates` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-mandates.md) for the provider-specific parameters and requirements.

