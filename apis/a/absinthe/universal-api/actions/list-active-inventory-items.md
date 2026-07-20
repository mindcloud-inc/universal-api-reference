# Absinthe: List Active Inventory Items

Retrieves active reward items from an Absinthe campaign.

```
GET https://connect.mindcloud.co/v1/universal/absinthe/latest/actions/list-active-inventory-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Absinthe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/absinthe/latest/actions/list-active-inventory-items?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/absinthe/latest/actions/list-active-inventory-items?${params}`, {
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
| `userId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Absinthe API returns.

## Native endpoint

Through the native Absinthe API, this operation is `GET /inventory/public` (base URL `https://api.absinthe.network`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-active-inventory-items.md) for the provider-specific parameters and requirements.

