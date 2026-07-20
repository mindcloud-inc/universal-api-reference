# NetExplorer: Update Group



```
PUT https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-group-by-group-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-group-by-group-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-group-by-group-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "ldap": true,
      "login": "string",
      "members": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Identifiant unique du groupe. |
| `ldap` | boolean | Indique si le groupe provient d'un annuaire externe. Attention Si ce champs vaut true, l'objet sera alors en lecture seule. |
| `login` | string | Nom du groupe. |
| `members` | string | Liste des membres du groupe. |

## Native endpoint

Through the native NetExplorer API, this operation is `PUT /group/:groupId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group-by-group-id.md) for the provider-specific parameters and requirements.

