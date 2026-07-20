# WotNot: Get Bot Flow

Retrieves a bot flow from WotNot.

```
GET https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/get-bot-flow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WotNot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/get-bot-flow?connectionId=$CONNECTION_ID&botId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/get-bot-flow?${params}`, {
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
| `botId` | number | yes | WotNot bot ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "is_deployed": true,
      "last_deployed_at": "2026-05-07T12:00:00.000Z",
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Serialized bot flow JSON. |
| `is_deployed` | boolean | Whether the flow is deployed. |
| `last_deployed_at` | date | Last deployment timestamp. |
| `ok` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native WotNot API, this operation is `GET /v1/bots/:bot_id/flow` (base URL `https://api.wotnot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bot-flow.md) for the provider-specific parameters and requirements.

