# Stiply: Cancel Sign Request

Cancels an existing Stiply sign request.

```
PUT https://connect.mindcloud.co/v1/universal/stiply/latest/actions/cancel-sign-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stiply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stiply/latest/actions/cancel-sign-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signRequest": 1,
  "notifySigners": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stiply/latest/actions/cancel-sign-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signRequest": 1,
    "notifySigners": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signRequest` | number | yes | Id of the signrequest. |
| `notifySigners` | boolean | yes | Provide whether the signers needs to be informed about the cancelation of the sign request. |
| `cancellationMessage` | string | no | Optional message to show the signers. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Stiply API returns.

## Native endpoint

Through the native Stiply API, this operation is `POST /v2/sign_requests/:sign_request/actions/cancel` (base URL `https://api.stiply.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-sign-request.md) for the provider-specific parameters and requirements.

