# NetExplorer: Create File



```
POST https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-template-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-template-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-template-file', {
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
      "date": "string",
      "description": "string",
      "fileType": "string",
      "guid": "string",
      "id": 1,
      "name": "Ava Chen",
      "parentId": 1,
      "thumbToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string | Date de modification du template. |
| `description` | string | Description du template. |
| `fileType` | string | Type d'aperçu du fichier. Peut valoir image, document ou video si l'aperçu est disponible pour ce fichier. |
| `guid` | string | guid du template. |
| `id` | number | Identifiant du template. |
| `name` | string | Nom du template. |
| `parentId` | number | Id du dossier parent du template. |
| `thumbToken` | string | Token d'accès aux miniatures de ce fichier si le format est supporté. |

## Native endpoint

Through the native NetExplorer API, this operation is `POST /template/file` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template-file.md) for the provider-specific parameters and requirements.

