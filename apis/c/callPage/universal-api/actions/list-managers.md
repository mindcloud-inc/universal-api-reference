# CallPage: List Managers

Retrieves all available managers from CallPage.

```
GET https://connect.mindcloud.co/v1/universal/callPage/latest/actions/list-managers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallPage `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callPage/latest/actions/list-managers?connectionId=$CONNECTION_ID&limit=25&offset=0&widgetId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "widgetId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callPage/latest/actions/list-managers?${params}`, {
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
| `widgetId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "business_times": [
        {}
      ],
      "departments": [
        {}
      ],
      "enabled": true,
      "id": 1,
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `business_times` | array<object> |  |
| `departments` | array<object> |  |
| `enabled` | boolean |  |
| `id` | number |  |
| `user` | object |  |

## Native endpoint

Through the native CallPage API, this operation is `GET /managers/all` (base URL `https://core.callpage.io/api/v1/external`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-managers.md) for the provider-specific parameters and requirements.

