# Aspire: Update Pay Rate



```
PUT https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-pay-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-pay-rate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "PayRateId": 1,
  "contactId": 1,
  "effectiveDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-pay-rate', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "PayRateId": 1,
    "contactId": 1,
    "effectiveDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `PayRateId` | list<number> | yes |  |
| `contactId` | list<number> | yes |  |
| `effectiveDate` | string | yes |  |
| `hourlyBasePay` | string | no |  |
| `burdenPercent` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "payRateID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `payRateID` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `PUT PayRates` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-pay-rate.md) for the provider-specific parameters and requirements.

