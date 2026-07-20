# LOBSTR.IO: Check Sync Status

Retrieves sync task status from LOBSTR.IO.

```
GET https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/check-sync-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LOBSTR.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/check-sync-status?connectionId=$CONNECTION_ID&syncTaskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "syncTaskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/check-sync-status?${params}`, {
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
| `syncTaskId` | string | yes | The synchronization task ID returned by Sync Account or Refresh Cookies. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountHash": "string",
      "id": "string",
      "object": "string",
      "statusCode": 1,
      "statusText": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountHash` | string |  |
| `id` | string |  |
| `object` | string |  |
| `statusCode` | number |  |
| `statusText` | string |  |

## Native endpoint

Through the native LOBSTR.IO API, this operation is `GET /v1/synchronize/:sync_task_id` (base URL `https://api.lobstr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-sync-status.md) for the provider-specific parameters and requirements.

