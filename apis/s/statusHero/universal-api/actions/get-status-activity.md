# Status Hero: Get status activity



```
GET https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/get-status-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Status Hero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/get-status-activity?connectionId=$CONNECTION_ID&id=status%20activity%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "status activity ID"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/get-status-activity?${params}`, {
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
| `id` | string | yes | The Status Hero status activity ID. Example: `status activity ID`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "htmlDescription": "string",
      "id": "string",
      "kind": "string",
      "statusId": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `htmlDescription` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `statusId` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Status Hero API, this operation is `GET /status_activities/:id` (base URL `https://service.statushero.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-status-activity.md) for the provider-specific parameters and requirements.

