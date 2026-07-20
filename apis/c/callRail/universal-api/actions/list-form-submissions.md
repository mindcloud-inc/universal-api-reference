# CallRail: List Form Submissions

Retrieves form submissions from CallRail.

```
GET https://connect.mindcloud.co/v1/universal/callRail/latest/actions/list-form-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallRail `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callRail/latest/actions/list-form-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0&account_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "account_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callRail/latest/actions/list-form-submissions?${params}`, {
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
| `account_id` | string | yes | The CallRail account ID. |
| `company_id` | string | no | Optional company ID to filter form submissions. |
| `date_range` | string | no | Standard CallRail date range filter. |
| `start_date` | string | no | Start of a custom date range in ISO 8601 format. |
| `end_date` | string | no | End of a custom date range in ISO 8601 format. |
| `person_lead` | boolean | no | Return only form submissions that have an associated lead when true. |
| `lead_status` | string | no | Filter submissions by lead status. |
| `tags` | string | no | Comma-separated tag names to match. |
| `fields` | string | no | Comma-separated response fields to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": "string",
      "companyId": "string",
      "customerEmail": "ava@example.com",
      "customerName": "Ava Chen",
      "customerPhoneNumber": "string",
      "firstForm": true,
      "formattedCustomerName": "Ava Chen",
      "formattedCustomerPhoneNumber": "string",
      "formData": {
        "emailAddress": "ava@example.com",
        "message": "string",
        "phoneNumber": "string",
        "textingConsent": "string",
        "yourName": "Ava Chen"
      },
      "formUrl": "https://example.com",
      "id": "string",
      "keywords": "string",
      "landingPageUrl": "https://example.com",
      "medium": "string",
      "personId": "string",
      "referrer": "string",
      "referringUrl": "https://example.com",
      "source": "string",
      "submittedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | string |  |
| `companyId` | string |  |
| `customerEmail` | string |  |
| `customerName` | string |  |
| `customerPhoneNumber` | string |  |
| `firstForm` | boolean |  |
| `formattedCustomerName` | string |  |
| `formattedCustomerPhoneNumber` | string |  |
| `formData` | object |  |
| `formData.emailAddress` | string |  |
| `formData.message` | string |  |
| `formData.phoneNumber` | string |  |
| `formData.textingConsent` | string |  |
| `formData.yourName` | string |  |
| `formUrl` | string |  |
| `id` | string |  |
| `keywords` | string |  |
| `landingPageUrl` | string |  |
| `medium` | string |  |
| `personId` | string |  |
| `referrer` | string |  |
| `referringUrl` | string |  |
| `source` | string |  |
| `submittedAt` | string |  |

## Native endpoint

Through the native CallRail API, this operation is `GET /v3/a/:account_id/form_submissions.json` (base URL `https://api.callrail.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-form-submissions.md) for the provider-specific parameters and requirements.

