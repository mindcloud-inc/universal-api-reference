# NetExplorer: Create App



```
POST https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-oauth2-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-oauth2-app" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-oauth2-app', {
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
      "clientId": "string",
      "clientSecret": "string",
      "description": "string",
      "editor": "string",
      "editorUrl": "https://example.com",
      "name": "Ava Chen",
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | string | Identifiant public de l'application fourni par NetExplorer. |
| `clientSecret` | string | Identifiant privée de l'application fourni par NetExplorer. Attention Cette information ne sera donnée qu'une seule fois à la création de l'application |
| `description` | string | Description de l'application. |
| `editor` | string | Éditeur de l'application. |
| `editorUrl` | string | Url de l'éditeur de l'application. |
| `name` | string | Nom de l'application. |
| `type` | number | Type d'application OAuth2 ValeurType 0Application Client Serveur |

## Native endpoint

Through the native NetExplorer API, this operation is `POST /oauth2/app` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-oauth2-app.md) for the provider-specific parameters and requirements.

