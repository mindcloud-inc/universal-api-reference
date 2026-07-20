# NetExplorer: Get App



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-oauth2-app-by-client-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-oauth2-app-by-client-id?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-oauth2-app-by-client-id?${params}`, {
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
| `clientId` | string | yes |  |

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

Through the native NetExplorer API, this operation is `GET /oauth2/app/:clientId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-oauth2-app-by-client-id.md) for the provider-specific parameters and requirements.

