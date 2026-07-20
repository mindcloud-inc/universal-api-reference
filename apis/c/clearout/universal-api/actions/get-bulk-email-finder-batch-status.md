# Clearout: Get Bulk Email Finder Batch Status

Retrieves bulk email finder batch status from Clearout.

```
GET https://connect.mindcloud.co/v1/universal/clearout/latest/actions/get-bulk-email-finder-batch-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clearout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearout/latest/actions/get-bulk-email-finder-batch-status?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clearout/latest/actions/get-bulk-email-finder-batch-status?${params}`, {
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
| `listId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "percentage": 1,
      "progressStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `percentage` | number |  |
| `progressStatus` | string |  |

## Native endpoint

Through the native Clearout API, this operation is `GET /email_finder/bulk/progress_status` (base URL `https://api.clearout.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-email-finder-batch-status.md) for the provider-specific parameters and requirements.

