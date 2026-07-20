# Clockify: Get Webhook Logs

Retrieves logs for a webhook from Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-webhook-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-webhook-logs?connectionId=$CONNECTION_ID&workspaceId=string&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-webhook-logs?${params}`, {
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
| `workspaceId` | list<string> | yes |  |
| `webhookId` | string<string> | yes |  |
| `from` | date | no | Example: `2026-01-01T00:00:00Z`. |
| `sortByNewest` | boolean | no | Example: `true`. |
| `status` | list<string> | no | One of: `ALL`, `FAILED`, `SUCCEEDED`. Example: `ACTIVE`. |
| `to` | date | no | Example: `2026-01-01T00:00:00Z`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `size` | number | no | Example: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "requestBody": "string",
      "respondedAt": "2026-05-07T12:00:00.000Z",
      "statusCode": 1,
      "webhookEventStatusId": "string",
      "webhookId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `requestBody` | string |  |
| `respondedAt` | date |  |
| `statusCode` | number |  |
| `webhookEventStatusId` | string |  |
| `webhookId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/webhooks/:webhookId/logs` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-logs.md) for the provider-specific parameters and requirements.

