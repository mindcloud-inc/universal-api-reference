# Sapling: Remove Custom Mapping

Deletes a custom mapping from Sapling.

```
DELETE https://connect.mindcloud.co/v1/universal/sapling/latest/actions/remove-custom-mapping
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sapling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sapling/latest/actions/remove-custom-mapping?connectionId=$CONNECTION_ID&customMappingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customMappingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sapling/latest/actions/remove-custom-mapping?${params}`, {
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
| `customMappingId` | string | yes | ID of the custom mapping to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sapling API returns.

## Native endpoint

Through the native Sapling API, this operation is `DELETE /api/v1/custom_mapping/:customMappingId` (base URL `https://api.sapling.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-custom-mapping.md) for the provider-specific parameters and requirements.

