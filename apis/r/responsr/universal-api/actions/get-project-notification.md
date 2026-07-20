# Responsr: Get Project Notification



```
GET https://connect.mindcloud.co/v1/universal/responsr/latest/actions/get-project-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Responsr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/responsr/latest/actions/get-project-notification?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/responsr/latest/actions/get-project-notification?${params}`, {
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
| `id` | string | no | Responsr notification ID. |
| `projectId` | string | no | Responsr project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "subject": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `subject` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Responsr API, this operation is `GET /api/v1.0/projects/:projectId/notifications/:id` (base URL `https://app.responsr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-notification.md) for the provider-specific parameters and requirements.

