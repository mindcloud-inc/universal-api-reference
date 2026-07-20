# NetExplorer: Create Annotation



```
POST https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-annotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-annotation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-annotation', {
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
      "conversation": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "owner": "string",
      "ownerId": "string",
      "targetId": 1,
      "targetType": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversation` | number | Identifiant unique de l'annotation dont ce message est la réponse. |
| `date` | date | Date à laquelle l'annotation a été créé. |
| `id` | number | Identifiant numérique unique de l'annotation. |
| `owner` | string | Nom complet de l'auteur de l'annotation. |
| `ownerId` | string | Identifiant unique de l'auteur de l'annotation. |
| `targetId` | number | Identifiant numérique unique du fichier ou du dossier. |
| `targetType` | string | Type d'objet rattaché. Vaut "file" ou "folder". |
| `text` | string | Contenu textuel de l'annotation |

## Native endpoint

Through the native NetExplorer API, this operation is `POST /annotation` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-annotation.md) for the provider-specific parameters and requirements.

