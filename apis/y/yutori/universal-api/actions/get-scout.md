# Yutori: Get Scout

Retrieves details for a specific scout in Yutori.

```
GET https://connect.mindcloud.co/v1/universal/yutori/latest/actions/get-scout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yutori `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yutori/latest/actions/get-scout?connectionId=$CONNECTION_ID&scoutId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scoutId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yutori/latest/actions/get-scout?${params}`, {
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
| `scoutId` | string | yes | The scout UUID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Yutori API returns.

## Native endpoint

Through the native Yutori API, this operation is `GET /v1/scouting/tasks/:scout_id` (base URL `https://api.yutori.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scout.md) for the provider-specific parameters and requirements.

