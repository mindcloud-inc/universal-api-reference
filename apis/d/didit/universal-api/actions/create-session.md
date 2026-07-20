# Didit: Create Session

Creates a new verification session in Didit.

```
POST https://connect.mindcloud.co/v1/universal/didit/latest/actions/create-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Didit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/didit/latest/actions/create-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/didit/latest/actions/create-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callback` | string | no | URL where Didit redirects the user after the session. |
| `callbackMethod` | string | no | Callback handling mode. Default: `initiator`. |
| `language` | string | no | Preferred session language code. Default: `en`. |
| `metadata` | string | no | Metadata string attached to the session. |
| `vendorData` | string | no | Your external reference for the session. |
| `workflowId` | string | yes | Workflow identifier configured in Didit. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sessionId": "string",
      "status": "string",
      "vendorData": "string",
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sessionId` | string |  |
| `status` | string |  |
| `vendorData` | string |  |
| `workflowId` | string |  |

## Native endpoint

Through the native Didit API, this operation is `POST https://verification.didit.me/v3/session/` (base URL `https://verification.didit.me/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-session.md) for the provider-specific parameters and requirements.

