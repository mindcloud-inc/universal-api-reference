# Stiply: Extend Sign Request Term

Extends the term of a Stiply sign request.

```
PUT https://connect.mindcloud.co/v1/universal/stiply/latest/actions/extend-sign-request-term
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stiply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stiply/latest/actions/extend-sign-request-term" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signRequest": 1,
  "term": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stiply/latest/actions/extend-sign-request-term', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signRequest": 1,
    "term": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signRequest` | number | yes | Id of the signrequest. |
| `term` | string | yes | 2 digit code representing the sign term (1d = one day, 2w = two weeks, 3m = three months). When omitted, the account's configured default term will be used. |
| `notifySigners` | boolean | no | Provide whether the signers needs to be informed about the extension of the term of the sign request. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Stiply API returns.

## Native endpoint

Through the native Stiply API, this operation is `POST /v2/sign_requests/:sign_request/actions/extend_term` (base URL `https://api.stiply.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extend-sign-request-term.md) for the provider-specific parameters and requirements.

