# United States Securities and Exchange Commission (SEC) EDGAR Database: Check Multiple Submission Statuses

Retrieves statuses for multiple EDGAR submissions.

```
GET https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/check-multiple-submission-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a United States Securities and Exchange Commission (SEC) EDGAR Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/check-multiple-submission-statuses?connectionId=$CONNECTION_ID&accessionNumbers%5B%5D=0000000000-26-000001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accessionNumbers[]": "0000000000-26-000001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/check-multiple-submission-statuses?${params}`, {
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
| `accessionNumbers[]` | array<string> | yes | Up to 25 EDGAR accession numbers to check. Example: `0000000000-26-000001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "locator": "string",
      "messages": [
        {}
      ],
      "responses": [
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
| `locator` | string | Short locator string for SEC support. |
| `messages` | array<object> | EDGAR response messages. |
| `responses` | array<object> | Submission status records for the requested accession numbers. |
| `tracking` | string | Universal tracking identifier for the EDGAR API request. |

## Native endpoint

Through the native United States Securities and Exchange Commission (SEC) EDGAR Database API, this operation is `POST https://api.edgarfiling.sec.gov/submission/status` (base URL `https://www.sec.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-multiple-submission-statuses.md) for the provider-specific parameters and requirements.

