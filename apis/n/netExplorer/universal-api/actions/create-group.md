# NetExplorer: Create Group



```
POST https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-group', {
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

Through the native NetExplorer API, this operation is `POST /group` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group.md) for the provider-specific parameters and requirements.

