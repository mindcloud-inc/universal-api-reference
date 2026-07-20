# United States Securities and Exchange Commission (SEC) EDGAR Database: Create Custom CCC

Updates a filer's CCC to a custom value in EDGAR.

```
PUT https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/create-custom-ccc
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a United States Securities and Exchange Commission (SEC) EDGAR Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/create-custom-ccc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cik": "0000320193",
  "ccc": "123456",
  "newCCC": "654321"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/create-custom-ccc', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cik": "0000320193",
    "ccc": "123456",
    "newCCC": "654321"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cik` | string | yes | 10-digit EDGAR account CIK. Example: `0000320193`. |
| `ccc` | string | yes | Current EDGAR CCC for the filer. Example: `123456`. |
| `newCCC` | string | yes | New custom EDGAR CCC to set for the filer. Example: `654321`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filerCCC": "string",
      "locator": "string",
      "messages": [
        {}
      ],
      "tracking": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filerCCC` | string | The custom CCC value now set for the filer. |
| `locator` | string | Short locator string for SEC support. |
| `messages` | array<object> | EDGAR response messages. |
| `tracking` | string | Universal tracking identifier for the EDGAR API request. |

## Native endpoint

Through the native United States Securities and Exchange Commission (SEC) EDGAR Database API, this operation is `PUT https://api.edgarfiling.sec.gov/fm/[:cik]/ccc` (base URL `https://www.sec.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-ccc.md) for the provider-specific parameters and requirements.

