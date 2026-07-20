# NetExplorer: Delete Email



```
DELETE https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/delete-sharelink-email-by-sharelink-email-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/delete-sharelink-email-by-sharelink-email-id?connectionId=$CONNECTION_ID&sharelinkEmailId=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sharelinkEmailId": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/delete-sharelink-email-by-sharelink-email-id?${params}`, {
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
| `sharelinkEmailId` | string | yes |  |

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

Through the native NetExplorer API, this operation is `DELETE /sharelink/email/:sharelinkEmailId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-sharelink-email-by-sharelink-email-id.md) for the provider-specific parameters and requirements.

