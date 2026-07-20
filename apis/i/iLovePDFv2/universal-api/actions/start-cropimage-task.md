# iLovePDFv2: Start Crop Image Task

Starts an image cropping task in iLovePDFv2.

```
POST https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/start-cropimage-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDFv2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/start-cropimage-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/start-cropimage-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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

Through the native iLovePDFv2 API, this operation is `GET https://api.iloveimg.com/v1/start/cropimage` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-cropimage-task.md) for the provider-specific parameters and requirements.

