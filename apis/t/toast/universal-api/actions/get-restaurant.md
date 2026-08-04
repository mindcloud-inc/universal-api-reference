# Toast: Get Restaurant



```
GET https://connect.mindcloud.co/v1/universal/toast/latest/actions/get-restaurant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toast/latest/actions/get-restaurant?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toast/latest/actions/get-restaurant?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeArchived` | boolean | no | Return the restaurant even when it is archived. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Toast API returns.

## Native endpoint

Through the native Toast API, this operation is `GET /restaurants/v1/restaurants/{{credentials.restaurantGuid}}` (base URL `{{credentials.connection}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-restaurant.md) for the provider-specific parameters and requirements.

