# NetExplorer: Get Activity



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-share-email-by-share-email-id-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-share-email-by-share-email-id-activity?connectionId=$CONNECTION_ID&shareEmailId=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shareEmailId": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-share-email-by-share-email-id-activity?${params}`, {
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
| `shareEmailId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nbObjects": 1,
      "nbTotalObjects": 1,
      "objects": [
        {
          "guid": "string",
          "name": "Ava Chen",
          "stats": [
            {
              "action": "string",
              "date": "2026-05-07T12:00:00.000Z",
              "email": "ava@example.com",
              "loc": "string"
            }
          ]
        }
      ],
      "offsetStart": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nbObjects` | number |  |
| `nbTotalObjects` | number |  |
| `objects` | array<object> |  |
| `objects[].guid` | string |  |
| `objects[].name` | string |  |
| `objects[].stats` | array<object> |  |
| `objects[].stats[].action` | string |  |
| `objects[].stats[].date` | date |  |
| `objects[].stats[].email` | string |  |
| `objects[].stats[].loc` | string |  |
| `offsetStart` | number |  |

## Native endpoint

Through the native NetExplorer API, this operation is `GET /share/email/:shareEmailId/activity` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-share-email-by-share-email-id-activity.md) for the provider-specific parameters and requirements.

