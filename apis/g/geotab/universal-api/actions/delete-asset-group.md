# Geotab: Delete Asset Group



```
DELETE https://connect.mindcloud.co/v1/universal/geotab/latest/actions/delete-asset-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geotab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/geotab/latest/actions/delete-asset-group?connectionId=$CONNECTION_ID&entity=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entity": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geotab/latest/actions/delete-asset-group?${params}`, {
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
| `entity` | object | yes | Group entity to remove. The object must contain its id. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Geotab API returns.

## Native endpoint

Through the native Geotab API, this operation is `POST` (base URL `https://{{credentials.server}}/apiv1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-asset-group.md) for the provider-specific parameters and requirements.

