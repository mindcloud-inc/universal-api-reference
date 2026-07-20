# ZeroBounce: Bulk Find Email File Status

Retrieves a bulk email finder file status from ZeroBounce.

```
GET https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/bulk-find-email-file-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZeroBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/bulk-find-email-file-status?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/bulk-find-email-file-status?${params}`, {
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
| `fileId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completePercentage": "string",
      "errorReason": "string",
      "fileId": "string",
      "fileName": "Ava Chen",
      "fileStatus": "string",
      "returnUrl": "https://example.com",
      "uploadDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completePercentage` | string | Completion percentage returned by ZeroBounce. |
| `errorReason` | string | Provider error reason when processing fails. |
| `fileId` | string | ZeroBounce file identifier. |
| `fileName` | string | Original uploaded file name. |
| `fileStatus` | string | Processing status for the bulk email finder file. |
| `returnUrl` | string | Configured callback URL when present. |
| `uploadDate` | date | Timestamp when ZeroBounce received the file. |

## Native endpoint

Through the native ZeroBounce API, this operation is `GET https://bulkapi.zerobounce.net/email-finder/filestatus` (base URL `https://api.zerobounce.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-find-email-file-status.md) for the provider-specific parameters and requirements.

