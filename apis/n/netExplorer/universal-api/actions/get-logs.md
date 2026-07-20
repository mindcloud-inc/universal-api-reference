# NetExplorer: List Logs



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-logs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "ip": "string",
      "message": "string",
      "object": "string",
      "objectId": "string",
      "objectType": "string",
      "statut": "string",
      "type": "string",
      "user": "string",
      "userAgent": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Date à laquelle l'évènement s'est produit. |
| `id` | number | Identifiant numérique unique de l'entrée des journaux. |
| `ip` | string | Adresse IP de connexion de l'utilisateur. |
| `message` | string | Informations complétaires spécifiques à l'évènement. |
| `object` | string | Nom représentatif de l'objet affecté. |
| `objectId` | string | Identifiant unique de l'élément affecté par la requête. |
| `objectType` | string | Type de l'objet affecté par la requête. |
| `statut` | string | Indique si l'évènement est un succès (ADMLLOG_OK) ou un échec (ADMLLOG_ERROR). |
| `type` | string | Type d'évènement enregistré. |
| `user` | string | Nom complet de l'utilisateur. |
| `userAgent` | string | Chaine d'identification du navigateur internet ou de l'outil utilisé pour la connexion. |
| `userId` | string | Identifiant unique de l'utilisateur à l'origine de l'action. Toute action de la part d'un utilisateur non connecté sera affichée comme provenant du compte Invité. |

## Native endpoint

Through the native NetExplorer API, this operation is `GET /logs` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-logs.md) for the provider-specific parameters and requirements.

