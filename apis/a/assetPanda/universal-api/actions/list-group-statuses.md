# Asset Panda: List Group Statuses

Retrieves group statuses from Asset Panda.

```
GET https://connect.mindcloud.co/v1/universal/assetPanda/latest/actions/list-group-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asset Panda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assetPanda/latest/actions/list-group-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assetPanda/latest/actions/list-group-statuses?${params}`, {
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
| `groupId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Asset Panda API returns.

## Native endpoint

Through the native Asset Panda API, this operation is `GET /v3/groups/:groupId/statuses` (base URL `https://api.assetpanda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-statuses.md) for the provider-specific parameters and requirements.

