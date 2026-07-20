# Aspire: Update Service Tax Override

Updates an existing service tax override in your Aspire account.

```
PUT https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-service-tax-override
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-service-tax-override" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stateProvinceCode": "string",
  "serviceTaxOverrideId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-service-tax-override', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stateProvinceCode": "string",
    "serviceTaxOverrideId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `serviceId` | number | no |  |
| `stateProvinceCode` | string | yes |  |
| `laborTaxable` | boolean | no |  |
| `materialTaxable` | boolean | no |  |
| `equipmentTaxable` | boolean | no |  |
| `subTaxable` | boolean | no |  |
| `otherTaxable` | boolean | no |  |
| `serviceTaxOverrideId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aspire API returns.

## Native endpoint

Through the native Aspire API, this operation is `PUT ServiceTaxOverrides` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-service-tax-override.md) for the provider-specific parameters and requirements.

