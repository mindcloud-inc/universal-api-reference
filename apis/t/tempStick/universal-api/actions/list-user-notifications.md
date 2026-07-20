# Temp Stick: List User Notifications

Retrieves the last seven days of Temp Stick user notifications.

```
GET https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/list-user-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Temp Stick `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/list-user-notifications?connectionId=$CONNECTION_ID&itemsPerPage=10&page=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemsPerPage": "10",
  "page": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/list-user-notifications?${params}`, {
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
| `itemsPerPage` | number | yes | Maximum 100 items per page Default: `10`. |
| `page` | number | yes | Page number Default: `0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Temp Stick API returns.

## Native endpoint

Through the native Temp Stick API, this operation is `GET /user/notifications` (base URL `https://tempstickapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-notifications.md) for the provider-specific parameters and requirements.

