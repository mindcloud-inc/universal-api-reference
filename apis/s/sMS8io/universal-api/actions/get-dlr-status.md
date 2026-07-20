# SMS8.io: Get DLR Status



```
GET https://connect.mindcloud.co/v1/universal/sMS8io/latest/actions/get-dlr-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS8.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMS8io/latest/actions/get-dlr-status?connectionId=$CONNECTION_ID&smsid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "smsid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMS8io/latest/actions/get-dlr-status?${params}`, {
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
| `smsid` | string | yes | SMS ID returned by the send endpoint. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMS8.io API returns.

## Native endpoint

Through the native SMS8.io API, this operation is `GET dlr/` (base URL `https://app.sms8.io/services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dlr-status.md) for the provider-specific parameters and requirements.

