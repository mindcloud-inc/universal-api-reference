# Aspire: Create Pay Rate

Creates a new pay code in your Aspire account.

```
POST https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-pay-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-pay-rate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "effectiveDate": "string",
  "hourlyBasePay": "https://example.com",
  "contactId": "string",
  "burdenPercent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-pay-rate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "effectiveDate": "string",
    "hourlyBasePay": "https://example.com",
    "contactId": "string",
    "burdenPercent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `effectiveDate` | string | yes |  |
| `hourlyBasePay` | string | yes |  |
| `contactId` | list<string> | yes |  |
| `burdenPercent` | string | yes |  |

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

Through the native Aspire API, this operation is `POST PayRates` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pay-rate.md) for the provider-specific parameters and requirements.

