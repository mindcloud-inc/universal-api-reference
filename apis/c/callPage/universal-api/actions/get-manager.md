# CallPage: Get Manager

Retrieves a single manager from CallPage.

```
GET https://connect.mindcloud.co/v1/universal/callPage/latest/actions/get-manager
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallPage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callPage/latest/actions/get-manager?connectionId=$CONNECTION_ID&userId=1&widgetId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "1",
  "widgetId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callPage/latest/actions/get-manager?${params}`, {
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
| `userId` | number | yes |  |
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

Through the native CallPage API, this operation is `GET /managers/get` (base URL `https://core.callpage.io/api/v1/external`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-manager.md) for the provider-specific parameters and requirements.

