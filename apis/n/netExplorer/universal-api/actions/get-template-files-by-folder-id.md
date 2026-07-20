# NetExplorer: List Template Files



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-template-files-by-folder-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-template-files-by-folder-id?connectionId=$CONNECTION_ID&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-template-files-by-folder-id?${params}`, {
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
| `folderId` | string | yes |  |

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

Through the native NetExplorer API, this operation is `GET /template/files/:folderId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-files-by-folder-id.md) for the provider-specific parameters and requirements.

