# Framework360: Update User



```
PUT https://connect.mindcloud.co/v1/universal/framework360/latest/actions/users-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Framework360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/framework360/latest/actions/users-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/framework360/latest/actions/users-update', {
  method: 'PUT',
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
| `citta` | string | no | User city. |
| `cognome` | string | no | User last name. |
| `email` | string | no | User email address. |
| `id` | string | no | User ID to update. |
| `indirizzo` | string | no | User address. |
| `marketing_list` | string | no | Marketing subscription flag. |
| `nome` | string | no | User first name. |
| `password` | string | no | New user password. |
| `stato` | string | no | User country. |
| `telefono` | string | no | User phone number. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Framework360 API returns.

## Native endpoint

Through the native Framework360 API, this operation is `POST users/update` (base URL `https://mindcloudstage0.framework360.site/m/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/users-update.md) for the provider-specific parameters and requirements.

