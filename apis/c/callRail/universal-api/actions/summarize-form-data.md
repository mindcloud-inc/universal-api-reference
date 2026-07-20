# CallRail: Summarize Form Data

Retrieves form summary data from CallRail.

```
GET https://connect.mindcloud.co/v1/universal/callRail/latest/actions/summarize-form-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallRail `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callRail/latest/actions/summarize-form-data?connectionId=$CONNECTION_ID&account_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "account_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callRail/latest/actions/summarize-form-data?${params}`, {
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
| `company_id` | string | no |  |
| `group_by` | string | no |  |
| `fields` | string<string> | no |  |
| `tags` | string | no | Comma-separated tag names to match. |
| `custom_form_ids` | string | no | Comma-separated custom form IDs to include. |
| `lead_status` | string | no | Filter summary results by lead status. |
| `date_range` | string | no | Standard CallRail date range filter. |
| `start_date` | string | no | Start of a custom date range in ISO 8601 format. |
| `end_date` | string | no | End of a custom date range in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": "string",
      "startDate": "string",
      "timeZone": "string",
      "totalResults": {
        "totalForms": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | string |  |
| `startDate` | string |  |
| `timeZone` | string |  |
| `totalResults` | object |  |
| `totalResults.totalForms` | number |  |

## Native endpoint

Through the native CallRail API, this operation is `GET /v3/a/:account_id/forms/summary.json` (base URL `https://api.callrail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/summarize-form-data.md) for the provider-specific parameters and requirements.

