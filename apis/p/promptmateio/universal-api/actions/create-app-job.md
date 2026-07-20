# Promptmate.io: Create App Job



```
POST https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/create-app-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Promptmate.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/create-app-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/create-app-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "data[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | The Promptmate app ID to run. |
| `noMailOnFinish` | boolean | no | Disable Promptmate completion emails for the job. |
| `data[]` | array<object> | yes | Array of input objects. Promptmate expects an array of single-key objects matching the app data-field labels, for example [{"Image URL":"https://example.com/test.png"}]. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callBackUrl` | string | no | Optional callback URL for job completion notifications. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "jobStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | Created Promptmate job ID. |
| `jobStatus` | string | Initial Promptmate job status. |

## Native endpoint

Through the native Promptmate.io API, this operation is `POST /app-jobs` (base URL `https://api.promptmate.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-app-job.md) for the provider-specific parameters and requirements.

