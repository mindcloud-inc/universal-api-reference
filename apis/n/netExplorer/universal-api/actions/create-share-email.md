# NetExplorer: Create Email



```
POST https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-share-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-share-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-share-email', {
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
      "content": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "object": "string",
      "ownerId": 1,
      "recipients": [
        {}
      ],
      "shareId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Contenu de l'email envoyé lors de la création du partage par email. |
| `creationDate` | date | Date à laquelle le partage par email a été crée. |
| `id` | number | Identifiant numérique unique du partage par email. |
| `object` | string | Objet envoyé lors de la création du partage par email. |
| `ownerId` | number | Identifiant numérique du créateur du partage par email. |
| `recipients` | array<object> | Tableau contenant les différents destinataires. Chaque entrées contient l'email du destinataire |
| `shareId` | number | Identifiant du partage par lien rattaché. |

## Native endpoint

Through the native NetExplorer API, this operation is `POST /share/email` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-share-email.md) for the provider-specific parameters and requirements.

