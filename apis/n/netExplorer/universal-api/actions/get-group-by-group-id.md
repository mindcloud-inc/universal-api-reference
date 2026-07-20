# NetExplorer: Get Group By Group ID



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-group-by-group-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-group-by-group-id?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-group-by-group-id?${params}`, {
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

Through the native NetExplorer API, this operation is `GET /group/:groupId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group-by-group-id.md) for the provider-specific parameters and requirements.

