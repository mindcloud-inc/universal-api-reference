# Climatiq: Estimate Emissions

Estimates emissions in Climatiq from activity data.

```
POST https://connect.mindcloud.co/v1/universal/climatiq/latest/actions/estimate-emissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Climatiq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/climatiq/latest/actions/estimate-emissions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emissionFactor": {},
  "parameters": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/climatiq/latest/actions/estimate-emissions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emissionFactor": {},
    "parameters": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emissionFactor` | object | yes | Emission factor selector object, such as activity_id and data_version. |
| `parameters` | object | yes | Activity data parameters object matching the selected factor unit type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activity_data": {},
      "additional_indicators": {},
      "audit_trail": "string",
      "co2e": 1,
      "co2e_calculation_method": "string",
      "co2e_calculation_origin": "string",
      "co2e_unit": "string",
      "constituent_gases": {},
      "emission_factor": {},
      "notices": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activity_data` | object | Activity value and unit used in the calculation. |
| `additional_indicators` | object | Supplementary indicator data. |
| `audit_trail` | string | Audit trail state for the response. |
| `co2e` | number | Calculated carbon dioxide equivalent. |
| `co2e_calculation_method` | string | Calculation method used for the estimate. |
| `co2e_calculation_origin` | string | Whether Climatiq or the source performed the calculation. |
| `co2e_unit` | string | Unit for the CO2e amount. |
| `constituent_gases` | object | Greenhouse gas breakdown for the estimate. |
| `emission_factor` | object | Emission factor used for the estimate. |
| `notices` | array<object> | Calculation notices. |

## Native endpoint

Through the native Climatiq API, this operation is `POST /data/v1/estimate` (base URL `https://api.climatiq.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/estimate-emissions.md) for the provider-specific parameters and requirements.

