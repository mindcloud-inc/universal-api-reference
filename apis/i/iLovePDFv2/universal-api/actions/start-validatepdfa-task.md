# iLovePDFv2: Start Validate PDF/A Task

Starts a PDF/A validation task in iLovePDFv2.

```
POST https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/start-validatepdfa-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDFv2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/start-validatepdfa-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "region": "us"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/start-validatepdfa-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "region": "us"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `region` | list | yes | Processing region / jurisdiction. One of: `0`, `1`, `2`, `3`, `4`. Default: `us`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "remaining_credits": 1,
      "remaining_files": 1,
      "server": "string",
      "task": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `remaining_credits` | number | Remaining credit allowance. |
| `remaining_files` | number | Remaining monthly file allowance. |
| `server` | string | Assigned iLoveAPI processing server. |
| `task` | string | Task identifier for upload/process/download calls. |

## Native endpoint

Through the native iLovePDFv2 API, this operation is `GET /start/validatepdfa/:region` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-validatepdfa-task.md) for the provider-specific parameters and requirements.

