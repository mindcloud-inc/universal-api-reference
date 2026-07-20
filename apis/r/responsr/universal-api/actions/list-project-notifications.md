# Responsr: List Project Notifications



```
GET https://connect.mindcloud.co/v1/universal/responsr/latest/actions/list-project-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Responsr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/responsr/latest/actions/list-project-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/responsr/latest/actions/list-project-notifications?${params}`, {
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
| `projectId` | string | no | Responsr project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "list": [
        {}
      ],
      "pagingInfo": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `list` | array<object> |  |
| `pagingInfo` | object |  |

## Native endpoint

Through the native Responsr API, this operation is `GET /api/v1.0/projects/:projectId/notifications` (base URL `https://app.responsr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-notifications.md) for the provider-specific parameters and requirements.

