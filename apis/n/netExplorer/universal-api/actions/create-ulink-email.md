# NetExplorer: Create Email



```
POST https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-ulink-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-ulink-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-ulink-email', {
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
      "alert": true,
      "content": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "folder": "string",
      "folderId": 1,
      "folderSize": 1,
      "id": 1,
      "object": "string",
      "ownerId": 1,
      "recipients": [
        {}
      ],
      "ulinkId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alert` | boolean | Le lien de dépôt a l'accusé de dépôt activé (flags 4 défini) |
| `content` | string | Contenu de l'email envoyé lors de la création du lien de dépôt par email. |
| `creationDate` | date | Date à laquelle le partage par email a été crée. |
| `folder` | string | Nom du dossier de destination. |
| `folderId` | number | Identifiant numérique unique du dossier dans lequel déposer les documents. Peut être défini à null si le dossier de destination n'existe plus. |
| `folderSize` | number | Taille du dossier de destination. |
| `id` | number | Identifiant numérique unique du lien de dépôt par email. |
| `object` | string | Objet envoyé lors de la création du lien de dépôt par email. |
| `ownerId` | number | Identifiant numérique du créateur du lien de dépôt par email. |
| `recipients` | array<object> | Tableau contenant les différents destinataires. Chaque entrées contient l'email du destinataire |
| `ulinkId` | number | Identifiant du lien de dépôt par lien rattaché. |

## Native endpoint

Through the native NetExplorer API, this operation is `POST /ulink/email` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ulink-email.md) for the provider-specific parameters and requirements.

