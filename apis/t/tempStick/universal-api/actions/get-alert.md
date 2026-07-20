# Temp Stick: Get Alert

Retrieves a specific alert from Temp Stick.

```
GET https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/get-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Temp Stick `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/get-alert?connectionId=$CONNECTION_ID&alertId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "alertId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/get-alert?${params}`, {
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
| `alertId` | number | yes | The ID of your alert |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Temp Stick API returns.

## Native endpoint

Through the native Temp Stick API, this operation is `GET /alerts/:alert_id` (base URL `https://tempstickapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alert.md) for the provider-specific parameters and requirements.

