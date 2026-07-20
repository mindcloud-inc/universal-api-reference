# United States Securities and Exchange Commission (SEC) EDGAR Database: Get EDGAR Operational Status

Retrieves the current EDGAR operational status.

```
GET https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-edgar-operational-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a United States Securities and Exchange Commission (SEC) EDGAR Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-edgar-operational-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-edgar-operational-status?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "condition": "string",
      "locator": "string",
      "message": "string",
      "tracking": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `condition` | string | Current EDGAR operational condition. |
| `locator` | string | Short locator string for SEC support. |
| `message` | string | Human-readable operational status message. |
| `tracking` | string | Universal tracking identifier for the EDGAR API request. |

## Native endpoint

Through the native United States Securities and Exchange Commission (SEC) EDGAR Database API, this operation is `GET https://api.edgarfiling.sec.gov/status` (base URL `https://www.sec.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-edgar-operational-status.md) for the provider-specific parameters and requirements.

