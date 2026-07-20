# Microsoft Power BI: Add Power BI Encryption Key



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-add-power-bi-encryption-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-add-power-bi-encryption-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-add-power-bi-encryption-key', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activate` | boolean | no | Whether to activate any inactivated capacities and to use this key for its encryption |
| `isDefault` | boolean | no | Whether an encryption key is the default key for the entire tenant. Any newly created capacity inherits the default key. |
| `keyVaultKeyIdentifier` | string | no | The URI that uniquely specifies an encryption key in Azure Key Vault |
| `name` | string | no | The name of the encryption key |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST admin/tenantKeys` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/admin-add-power-bi-encryption-key.md) for the provider-specific parameters and requirements.

