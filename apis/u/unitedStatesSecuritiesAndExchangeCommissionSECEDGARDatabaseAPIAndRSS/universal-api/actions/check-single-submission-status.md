# United States Securities and Exchange Commission (SEC) EDGAR Database: Check Single Submission Status

Retrieves the status of a single EDGAR submission.

```
GET https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/check-single-submission-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a United States Securities and Exchange Commission (SEC) EDGAR Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/check-single-submission-status?connectionId=$CONNECTION_ID&accessionNumber=0000000000-26-000001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accessionNumber": "0000000000-26-000001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/check-single-submission-status?${params}`, {
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
| `accessionNumber` | string | yes | EDGAR accession number to check. Example: `0000000000-26-000001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptedDate": "2026-05-07T12:00:00.000Z",
      "accessionNumber": "string",
      "classInformation": [
        {}
      ],
      "company": "string",
      "documentCount": 1,
      "fileNumbers": [
        "string"
      ],
      "filingDate": "2026-05-07T12:00:00.000Z",
      "final": true,
      "formType": "string",
      "items": [
        "string"
      ],
      "locator": "string",
      "messages": [
        {}
      ],
      "mode": {},
      "notification": "string",
      "receivedDate": "2026-05-07T12:00:00.000Z",
      "registrants": [
        {}
      ],
      "seriesInformation": [
        {}
      ],
      "status": "string",
      "submissionAccessionNumber": "string",
      "submissionFormType": "string",
      "submissionMessages": [
        {}
      ],
      "submissionProcessingStatus": "string",
      "suspendedDate": "2026-05-07T12:00:00.000Z",
      "tracking": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptedDate` | date | Date the submission was accepted. |
| `accessionNumber` | string | Primary accession number for the submission. |
| `classInformation` | array<object> | Class-level information returned by EDGAR. |
| `company` | string | Company name for the submission. |
| `documentCount` | number | Number of documents in the submission. |
| `fileNumbers` | array<string> | SEC file numbers on the submission. |
| `filingDate` | date | Official filing date. |
| `final` | boolean | Whether the submission status is final. |
| `formType` | string | Form type in the submission. |
| `items` | array<string> | Associated EDGAR item codes. |
| `locator` | string | Short locator string for SEC support. |
| `messages` | array<object> | EDGAR response messages. |
| `mode` | object | Submission mode metadata. |
| `notification` | string | Notification text returned by EDGAR. |
| `receivedDate` | date | Date EDGAR received the submission. |
| `registrants` | array<object> | Registrant records on the submission. |
| `seriesInformation` | array<object> | Series-level information returned by EDGAR. |
| `status` | string | Current EDGAR submission status. |
| `submissionAccessionNumber` | string | Submission accession number associated with item submissions. |
| `submissionFormType` | string | Submission form type. |
| `submissionMessages` | array<object> | Processing messages associated with the submission. |
| `submissionProcessingStatus` | string | Processing status category returned by EDGAR. |
| `suspendedDate` | date | Date the submission was suspended, if any. |
| `tracking` | string | Universal tracking identifier for the EDGAR API request. |

## Native endpoint

Through the native United States Securities and Exchange Commission (SEC) EDGAR Database API, this operation is `GET https://api.edgarfiling.sec.gov/submission/[:accessionNumber]/status` (base URL `https://www.sec.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-single-submission-status.md) for the provider-specific parameters and requirements.

