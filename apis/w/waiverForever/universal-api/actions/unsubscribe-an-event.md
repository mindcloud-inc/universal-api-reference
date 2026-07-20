# WaiverForever: Unsubscribe an Event

Deletes a webhook subscription from WaiverForever.

```
DELETE https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/unsubscribe-an-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/unsubscribe-an-event?connectionId=$CONNECTION_ID&subscriptionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriptionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/unsubscribe-an-event?${params}`, {
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
| `subscriptionId` | string | yes | Webhook subscription identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "msg": "string",
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `msg` | string | Provider response message. |
| `result` | boolean | Whether the unsubscribe request succeeded. |

## Native endpoint

Through the native WaiverForever API, this operation is `DELETE /openapi/v1/webhooks/:subscription_id/` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-an-event.md) for the provider-specific parameters and requirements.

