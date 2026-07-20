# NetExplorer: Get Email



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-shares-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-shares-emails?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-shares-emails?${params}`, {
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

Through the native NetExplorer API, this operation is `GET /shares/emails` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shares-emails.md) for the provider-specific parameters and requirements.

