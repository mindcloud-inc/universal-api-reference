# ServiceM8: Create Client



```
POST https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceM8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Company name. |
| `website` | string | no | Website URL. |
| `address` | string | no | Primary address. |
| `addressStreet` | string | no | Street address. |
| `addressCity` | string | no | Address city. |
| `addressState` | string | no | Address state. |
| `addressPostcode` | string | no | Address postcode. |
| `addressCountry` | string | no | Address country. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billingAddress` | string | no | Billing address. |
| `billingAttention` | string | no | Billing attention line. |
| `paymentTerms` | string | no | Payment terms. |
| `abnNumber` | string | no | Australian Business Number. |
| `faxNumber` | string | no | Fax number. |
| `taxRateUuid` | string | no | Tax rate UUID. |
| `parentCompanyUuid` | string | no | Parent company UUID for site records. |
| `badges` | string | no | JSON array of badge UUIDs. |
| `uuid` | string | no | Optional record UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "recordUuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `recordUuid` | string | UUID of the created client. |

## Native endpoint

Through the native ServiceM8 API, this operation is `POST /api_1.0/company.json` (base URL `https://api.servicem8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

