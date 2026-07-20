# NetExplorer: Get Email



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-sharelinks-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-sharelinks-emails?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-sharelinks-emails?${params}`, {
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
      "id": 1,
      "object": "string",
      "owner": 1,
      "recipients": [
        {}
      ],
      "sendingDate": "2026-05-07T12:00:00.000Z",
      "stats": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Contenu de l'email envoyé lors de la création du partage par email. |
| `id` | number | Identifiant numérique unique du partage par email. |
| `object` | string | Objet envoyé lors de la création du partage par email. |
| `owner` | number | Identifiant numérique du créateur du partage par email. |
| `recipients` | array<object> | Tableau contenant les différents destinataires. Chaque entrées contient email name du destinataire Si le destinataire est une persone interne la propriété id sera rajouté. La propriété dlink correspondra au partage par lien (unique) du destinataire. |
| `sendingDate` | date | Date à laquelle l'email a été envoyé. |
| `stats` | object | Statistiques des téléchargements et des aperçus du partage par email. |

## Native endpoint

Through the native NetExplorer API, this operation is `GET /sharelinks/emails` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sharelinks-emails.md) for the provider-specific parameters and requirements.

