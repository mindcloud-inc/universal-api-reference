# United States Securities and Exchange Commission (SEC) EDGAR Database: Get Delegations

Retrieves delegation relationships for an EDGAR filer account.

```
GET https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-delegations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a United States Securities and Exchange Commission (SEC) EDGAR Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-delegations?connectionId=$CONNECTION_ID&cik=0000320193" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cik": "0000320193"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-delegations?${params}`, {
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
| `cik` | string | yes | 10-digit EDGAR account CIK. Example: `0000320193`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "delegationsFrom": [
        {}
      ],
      "delegationsTo": [
        {}
      ],
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
| `delegationsFrom` | array<object> | Delegations received from other EDGAR accounts. |
| `delegationsTo` | array<object> | Delegations granted to other EDGAR accounts. |
| `locator` | string | Short locator string for SEC support. |
| `messages` | array<object> | EDGAR response messages. |
| `tracking` | string | Universal tracking identifier for the EDGAR API request. |

## Native endpoint

Through the native United States Securities and Exchange Commission (SEC) EDGAR Database API, this operation is `GET https://api.edgarfiling.sec.gov/fm/[:cik]/delegations` (base URL `https://www.sec.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-delegations.md) for the provider-specific parameters and requirements.

