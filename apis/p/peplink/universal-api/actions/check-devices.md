# Peplink: Check Devices



```
GET https://connect.mindcloud.co/v1/universal/peplink/latest/actions/check-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peplink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peplink/latest/actions/check-devices?connectionId=$CONNECTION_ID&sns=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sns": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peplink/latest/actions/check-devices?${params}`, {
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
| `sns` | string | yes | Enter serial numbers of devices to find. Use , as separator for multiple serial numbers. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Peplink API returns.

## Native endpoint

Through the native Peplink API, this operation is `GET devices/check` (base URL `https://portal.peplink.com/api/e/v1/cp/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-devices.md) for the provider-specific parameters and requirements.

