# IceCubes: List Action Items



```
GET https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/list-action-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IceCubes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/list-action-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/list-action-items?${params}`, {
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
| `meetingId` | string | no | Filter action items by meeting ID. |
| `completed` | boolean | no | Filter by completion status. |
| `tag` | string | no | Filter by tag name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionItems": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionItems` | array<object> | List of action items. |
| `pagination` | object | Pagination metadata for the action item list. |

## Native endpoint

Through the native IceCubes API, this operation is `GET /action-items` (base URL `https://icecubes.app/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-action-items.md) for the provider-specific parameters and requirements.

