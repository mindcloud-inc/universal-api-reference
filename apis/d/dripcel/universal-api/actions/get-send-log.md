# Dripcel: Get Send Log

Retrieves a send log from Dripcel by ID.

```
GET https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/get-send-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dripcel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/get-send-log?connectionId=$CONNECTION_ID&sendId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sendId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/get-send-log?${params}`, {
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
| `sendId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dripcel API returns.

## Native endpoint

Through the native Dripcel API, this operation is `GET /send-logs/:send_id` (base URL `https://api.dripcel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-send-log.md) for the provider-specific parameters and requirements.

