# Salesforce: Get Deleted Quote Line Items



```
GET https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/get-deleted-quote-line-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/get-deleted-quote-line-items?connectionId=$CONNECTION_ID&start=2026-11-01T00%3A00%3A00Z&end=2026-11-01T00%3A00%3A00Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "2026-11-01T00:00:00Z",
  "end": "2026-11-01T00:00:00Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/get-deleted-quote-line-items?${params}`, {
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
| `start` | date | yes | UTC timestamp. Salesforce ignores seconds and only retains recent deletion coverage (up to 15 days). Example: `2026-11-01T00:00:00Z`. |
| `end` | date | yes | UTC timestamp. Salesforce ignores seconds and only retains recent deletion coverage (up to 15 days). Example: `2026-11-01T00:00:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedRecords": [
        {
          "id": "string",
          "deletedDate": "string"
        }
      ],
      "earliestDateAvailable": "string",
      "latestDateCovered": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedRecords` | array<object> | Provisional documentation-based field; runtime confirmation pending. |
| `deletedRecords[].id` | string | Provisional documentation-based field; runtime confirmation pending. |
| `deletedRecords[].deletedDate` | string | Provisional documentation-based field; runtime confirmation pending. |
| `earliestDateAvailable` | string | Provisional documentation-based field; runtime confirmation pending. |
| `latestDateCovered` | string | Provisional documentation-based field; runtime confirmation pending. |

## Native endpoint

Through the native Salesforce API, this operation is `GET /services/data/v61.0/sobjects/QuoteLineItem/deleted/` (base URL `https://{{credentials.companyDomainName}}.my.salesforce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deleted-quote-line-items.md) for the provider-specific parameters and requirements.

