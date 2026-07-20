# ThriveDesk: Get Inbox Automation



```
GET https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-inbox-automation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThriveDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-inbox-automation?connectionId=$CONNECTION_ID&automationId=string&inboxId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "automationId": "string",
  "inboxId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-inbox-automation?${params}`, {
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
| `automationId` | string | yes | The automation ID. |
| `inboxId` | string | yes | The inbox ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Raw response payload. |
| `id` | string | Automation identifier when returned. |
| `message` | string | Provider response message when returned. |
| `name` | string | Automation name when returned. |
| `status` | string | Automation status when returned. |

## Native endpoint

Through the native ThriveDesk API, this operation is `GET /v1/inboxes/{{inboxId}}/automations/{{automationId}}` (base URL `https://api.thrivedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inbox-automation.md) for the provider-specific parameters and requirements.

