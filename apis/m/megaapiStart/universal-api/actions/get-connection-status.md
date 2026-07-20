# Megaapi Start: Get Connection Status

Retrieves WhatsApp connection status from Megaapi Start.

```
GET https://connect.mindcloud.co/v1/universal/megaapiStart/latest/actions/get-connection-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Megaapi Start `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/megaapiStart/latest/actions/get-connection-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/megaapiStart/latest/actions/get-connection-status?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Megaapi Start API returns.

## Native endpoint

Through the native Megaapi Start API, this operation is `GET /rest/instance/:instance_key` (base URL `https://{{credentials.host}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connection-status.md) for the provider-specific parameters and requirements.

