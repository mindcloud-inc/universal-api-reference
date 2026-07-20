# Hightouch: List Decision Engine Messages

Retrieves decision engine messages from Hightouch.

```
GET https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/list-decision-engine-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/list-decision-engine-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&flowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "flowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/list-decision-engine-messages?${params}`, {
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
| `flowId` | string | yes | The Decision Engine flow ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "hasMore": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Decision engine message records returned by Hightouch. |
| `hasMore` | boolean | Whether more results are available. |

## Native endpoint

Through the native Hightouch API, this operation is `GET /decision-engine/flow/{flowId}/messages` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-decision-engine-messages.md) for the provider-specific parameters and requirements.

