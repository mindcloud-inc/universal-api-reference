# AWeber: Get Subscriber

Retrieves a subscriber from AWeber.

```
GET https://connect.mindcloud.co/v1/universal/aWeber/latest/actions/get-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AWeber `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aWeber/latest/actions/get-subscriber?connectionId=$CONNECTION_ID&accountId=string&listId=string&subscriberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "listId": "string",
  "subscriberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aWeber/latest/actions/get-subscriber?${params}`, {
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
| `accountId` | string | yes |  |
| `listId` | string | yes |  |
| `subscriberId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AWeber API returns.

## Native endpoint

Through the native AWeber API, this operation is `GET /accounts/:accountId/lists/:listId/subscribers/:subscriberId` (base URL `https://api.aweber.com/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber.md) for the provider-specific parameters and requirements.

