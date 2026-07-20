# MindStudio: Run App

Runs an app in MindStudio.

```
POST https://connect.mindcloud.co/v1/universal/mindStudio/latest/actions/run-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MindStudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mindStudio/latest/actions/run-app" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mindStudio/latest/actions/run-app', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | The MindStudio app ID to run. |
| `variables` | object | no | Variables to pass into the MindStudio app run. |
| `workflow` | string | no | Optional workflow to run within the app. |
| `callbackUrl` | string | no | Optional callback URL for asynchronous app runs. |
| `includeBillingCost` | boolean | no | Whether to include billing cost information in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingCost": "string",
      "callbackInProgress": true,
      "result": {},
      "success": true,
      "thread": {},
      "threadId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingCost` | string | Billing cost returned when requested. |
| `callbackInProgress` | boolean | Whether the run is continuing asynchronously via callback. |
| `result` | object | The app result payload when the run completes synchronously. |
| `success` | boolean | Whether the callback-based run request was accepted. |
| `thread` | object | Thread details returned for the app run. |
| `threadId` | string | The thread ID created for the app run. |

## Native endpoint

Through the native MindStudio API, this operation is `POST /apps/run` (base URL `https://api.mindstudio.ai/developer/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-app.md) for the provider-specific parameters and requirements.

