# Deftform: List Form Responses

Retrieves responses for a form from Deftform.

```
GET https://connect.mindcloud.co/v1/universal/deftform/latest/actions/list-form-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deftform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deftform/latest/actions/list-form-responses?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deftform/latest/actions/list-form-responses?${params}`, {
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
| `formId` | string | yes | The Deftform form ID, available from the form detail page or the List Forms action. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "enrich": true,
      "google_sheets_sync": true,
      "google_sheets_synced_at": "2026-05-07T12:00:00.000Z",
      "hubspot_sync": true,
      "hubspot_sync_completed": true,
      "number": 1,
      "number_formatted": "string",
      "referrer": "string",
      "responses": [
        {}
      ],
      "uuid": "string",
      "webhook_sent": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Submission creation timestamp. |
| `enrich` | boolean | Whether enrichment is enabled for the submission. |
| `google_sheets_sync` | boolean | Whether Google Sheets sync is enabled. |
| `google_sheets_synced_at` | date | Google Sheets sync timestamp or null. |
| `hubspot_sync` | boolean | Whether HubSpot sync is enabled. |
| `hubspot_sync_completed` | boolean | Whether HubSpot sync completed. |
| `number` | number | Submission number within the form. |
| `number_formatted` | string | Formatted submission number. |
| `referrer` | string | Submission referrer or null. |
| `responses` | array<object> | Submitted field responses as key/value objects. |
| `uuid` | string | Unique submission UUID. |
| `webhook_sent` | boolean | Whether a webhook was sent. |

## Native endpoint

Through the native Deftform API, this operation is `GET /responses/:formId` (base URL `https://deftform.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-responses.md) for the provider-specific parameters and requirements.

