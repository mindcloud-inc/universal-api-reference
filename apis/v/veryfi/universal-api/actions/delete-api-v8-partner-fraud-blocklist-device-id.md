# Veryfi: Remove a device from blocklist

Removes a device from Veryfi's blocklist.

```
DELETE https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/delete-api-v8-partner-fraud-blocklist-device-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/delete-api-v8-partner-fraud-blocklist-device-id?connectionId=$CONNECTION_ID&deviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/delete-api-v8-partner-fraud-blocklist-device-id?${params}`, {
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
| `deviceId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Veryfi API returns.

## Native endpoint

Through the native Veryfi API, this operation is `DELETE /api/v8/partner/fraud/blocklist/:device_id` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-api-v8-partner-fraud-blocklist-device-id.md) for the provider-specific parameters and requirements.

