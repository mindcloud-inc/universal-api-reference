# Placker: List Cards On List



```
GET https://connect.mindcloud.co/v1/universal/placker/latest/actions/list-cards-on-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placker/latest/actions/list-cards-on-list?connectionId=$CONNECTION_ID&list=1235" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "list": "1235"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placker/latest/actions/list-cards-on-list?${params}`, {
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
| `list` | number | yes | List ID. Example: `1235`. |
| `includeArchived` | boolean | no | Include archived cards in results. Example: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Placker API returns.

## Native endpoint

Through the native Placker API, this operation is `GET /list/:list/card` (base URL `https://api.placker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cards-on-list.md) for the provider-specific parameters and requirements.

