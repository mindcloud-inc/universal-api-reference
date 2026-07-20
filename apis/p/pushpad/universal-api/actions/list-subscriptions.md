# Pushpad: List Subscriptions

Retrieves subscriptions from a Pushpad project.

```
GET https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/list-subscriptions?${params}`, {
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
| `page` | number | no |  |
| `perPage` | number | no |  |
| `projectId` | number | yes |  |
| `tags[]` | array<string> | no | Accepts multiple values as an array. |
| `uids[]` | array<string> | no | Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auth": "string",
      "createdAt": "string",
      "endpoint": "string",
      "id": 1,
      "lastClickAt": "string",
      "p256dh": "string",
      "projectId": 1,
      "tags": [
        "string"
      ],
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auth` | string |  |
| `createdAt` | string |  |
| `endpoint` | string |  |
| `id` | number |  |
| `lastClickAt` | string |  |
| `p256dh` | string |  |
| `projectId` | number |  |
| `tags` | array<string> |  |
| `uid` | string |  |

## Native endpoint

Through the native Pushpad API, this operation is `GET /projects/:project_id/subscriptions` (base URL `https://pushpad.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

