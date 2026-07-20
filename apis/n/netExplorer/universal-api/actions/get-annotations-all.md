# NetExplorer: Get All



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-annotations-all
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-annotations-all?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-annotations-all?${params}`, {
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

Through the native NetExplorer API, this operation is `GET /annotations/all` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-annotations-all.md) for the provider-specific parameters and requirements.

