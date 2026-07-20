# Framework360: Update Customer



```
PUT https://connect.mindcloud.co/v1/universal/framework360/latest/actions/customers-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Framework360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/framework360/latest/actions/customers-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/framework360/latest/actions/customers-update', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Customer ID to update. |
| `nome` | string | no | Customer first name. |
| `cognome` | string | no | Customer last name. |
| `email` | string | no | Customer email address. |
| `password` | string | no | New customer password. |
| `telefono` | string | no | Customer phone number. |
| `companyName` | string | no | Billing company name. |
| `vatNumber` | string | no | VAT number. |
| `taxCode` | string | no | Tax code. |
| `pec` | string | no | Certified email address. |
| `sdiCode` | string | no | SDI code. |
| `billingAddress` | string | no | Billing address. |
| `country` | string | no | Country. |
| `city` | string | no | City. |
| `municipality` | string | no | Municipality. |
| `postalCode` | string | no | Postal code. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Framework360 API returns.

## Native endpoint

Through the native Framework360 API, this operation is `POST customers/update` (base URL `https://mindcloudstage0.framework360.site/m/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/customers-update.md) for the provider-specific parameters and requirements.

