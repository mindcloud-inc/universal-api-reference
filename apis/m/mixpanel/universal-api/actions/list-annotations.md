# Mixpanel: List Annotations

Retrieves annotations from a Mixpanel project.

```
GET https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/list-annotations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mixpanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/list-annotations?connectionId=$CONNECTION_ID&projectId=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/list-annotations?${params}`, {
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
| `projectId` | number | yes | Mixpanel project ID. Example: `12345`. |
| `fromDate` | string | no | Inclusive start date in YYYY-MM-DD format. Example: `2026-03-01`. |
| `toDate` | string | no | Inclusive end date in YYYY-MM-DD format. Example: `2026-03-12`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        [
          "string"
        ]
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results[]` | array<string> |  |
| `status` | string |  |

## Native endpoint

Through the native Mixpanel API, this operation is `GET /app/projects/:projectId/annotations` (base URL `https://mixpanel.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-annotations.md) for the provider-specific parameters and requirements.

