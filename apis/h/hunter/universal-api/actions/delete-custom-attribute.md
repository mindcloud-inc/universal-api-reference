# Hunter: Delete Custom Attribute



```
DELETE https://connect.mindcloud.co/v1/universal/hunter/latest/actions/delete-custom-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/delete-custom-attribute?connectionId=$CONNECTION_ID&customAttributeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customAttributeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hunter/latest/actions/delete-custom-attribute?${params}`, {
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
| `customAttributeId` | string | yes | Identifier of the custom attribute. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Hunter API returns.

## Native endpoint

Through the native Hunter API, this operation is `DELETE /leads_custom_attributes/:customAttributeId` (base URL `https://api.hunter.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-custom-attribute.md) for the provider-specific parameters and requirements.

