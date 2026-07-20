# Avionte: Get a Talent Nomination Stage



```
GET https://connect.mindcloud.co/v1/universal/avionte/latest/actions/get-a-talent-nomination-stage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avionte `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avionte/latest/actions/get-a-talent-nomination-stage?connectionId=$CONNECTION_ID&nominationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "nominationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avionte/latest/actions/get-a-talent-nomination-stage?${params}`, {
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
| `nominationId` | number | yes | The Avionte nomination stage identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avionte API returns.

## Native endpoint

Through the native Avionte API, this operation is `GET front-office/v1/talent/stage/:nominationId` (base URL `https://api.avionte.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-talent-nomination-stage.md) for the provider-specific parameters and requirements.

