# Adafruit IO: Get Action

Retrieves an action from Adafruit IO.

```
GET https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/get-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adafruit IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/get-action?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adafruitIO/latest/actions/get-action?${params}`, {
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
| `id` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Adafruit IO API returns.

## Native endpoint

Through the native Adafruit IO API, this operation is `GET /{{credentials.username}}/actions/:id` (base URL `https://io.adafruit.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-action.md) for the provider-specific parameters and requirements.

