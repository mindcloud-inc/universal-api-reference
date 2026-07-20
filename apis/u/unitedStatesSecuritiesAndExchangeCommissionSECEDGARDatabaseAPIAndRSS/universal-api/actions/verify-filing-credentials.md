# United States Securities and Exchange Commission (SEC) EDGAR Database: Verify Filing Credentials

Retrieves filing credential verification results from the EDGAR API.

```
GET https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/verify-filing-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a United States Securities and Exchange Commission (SEC) EDGAR Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/verify-filing-credentials?connectionId=$CONNECTION_ID&cik=0000320193" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cik": "0000320193"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/verify-filing-credentials?${params}`, {
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
      "canFile": true,
      "confirmationDueDate": "2026-05-07T12:00:00.000Z",
      "filerApiTokenExpirationDate": "2026-05-07T12:00:00.000Z",
      "locator": "string",
      "messages": [
        {}
      ],
      "tracking": "string",
      "userApiTokenExpirationDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canFile` | boolean | Whether the provided credentials can file for the target CIK. |
| `confirmationDueDate` | date | Annual confirmation due date for the filer. |
| `filerApiTokenExpirationDate` | date | Expiration date for the filer API token. |
| `locator` | string | Short locator string for SEC support. |
| `messages` | array<object> | EDGAR response messages. |
| `tracking` | string | Universal tracking identifier for the EDGAR API request. |
| `userApiTokenExpirationDate` | date | Expiration date for the user API token. |

## Native endpoint

Through the native United States Securities and Exchange Commission (SEC) EDGAR Database API, this operation is `GET https://api.edgarfiling.sec.gov/fm/[:cik]/verify` (base URL `https://www.sec.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-filing-credentials.md) for the provider-specific parameters and requirements.

