# Webex Interact: Cancel scheduled SMS request

Cancels a scheduled SMS request in Webex Interact.

```
DELETE https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/cancel-scheduled-sms-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex Interact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/cancel-scheduled-sms-request?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/cancel-scheduled-sms-request?${params}`, {
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
| `id` | string | yes | Campaign or API SMS request ID to cancel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status_code": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `status_code` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Webex Interact API, this operation is `DELETE /campaigns/v1/cancel/{id}` (base URL `https://api.webexinteract.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-scheduled-sms-request.md) for the provider-specific parameters and requirements.

