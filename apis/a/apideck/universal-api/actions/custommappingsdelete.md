# Apideck: Delete custom mapping

Deletes an existing custom mapping from Apideck Vault.

```
DELETE https://connect.mindcloud.co/v1/universal/apideck/latest/actions/custommappingsdelete
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apideck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/apideck/latest/actions/custommappingsdelete?connectionId=$CONNECTION_ID&unified_api=string&service_id=string&target_field_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "unified_api": "string",
  "service_id": "string",
  "target_field_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apideck/latest/actions/custommappingsdelete?${params}`, {
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
| `unified_api` | string | yes |  |
| `service_id` | string | yes |  |
| `target_field_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string |  |

## Native endpoint

Through the native Apideck API, this operation is `DELETE /vault/custom-mappings/:unified_api/:service_id/:target_field_id` (base URL `https://unify.apideck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/custommappingsdelete.md) for the provider-specific parameters and requirements.

