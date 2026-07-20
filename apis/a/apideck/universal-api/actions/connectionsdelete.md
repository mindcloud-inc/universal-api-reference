# Apideck: Delete connection

Deletes an existing connection from Apideck Vault.

```
DELETE https://connect.mindcloud.co/v1/universal/apideck/latest/actions/connectionsdelete
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apideck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/apideck/latest/actions/connectionsdelete?connectionId=$CONNECTION_ID&service_id=string&unified_api=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "service_id": "string",
  "unified_api": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apideck/latest/actions/connectionsdelete?${params}`, {
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
| `service_id` | string | yes |  |
| `unified_api` | string | yes |  |

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

Through the native Apideck API, this operation is `DELETE /vault/connections/:unified_api/:service_id` (base URL `https://unify.apideck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/connectionsdelete.md) for the provider-specific parameters and requirements.

