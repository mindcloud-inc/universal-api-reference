# iLoveSign: Get Receiver Info



```
GET https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/get-receiver-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLoveSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/get-receiver-info?connectionId=$CONNECTION_ID&receiverTokenRequester=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "receiverTokenRequester": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/get-receiver-info?${params}`, {
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
| `receiverTokenRequester` | string | yes | Receiver token requester identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native iLoveSign API returns.

## Native endpoint

Through the native iLoveSign API, this operation is `GET /signature/receiver/info/:receiver_token_requester` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-receiver-info.md) for the provider-specific parameters and requirements.

