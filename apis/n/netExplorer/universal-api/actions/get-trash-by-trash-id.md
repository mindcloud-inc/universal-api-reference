# NetExplorer: Get Trash By Trash ID



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-trash-by-trash-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-trash-by-trash-id?connectionId=$CONNECTION_ID&trashId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trashId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-trash-by-trash-id?${params}`, {
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
| `trashId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletion": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isFile": true,
      "modification": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "nbFiles": 1,
      "nbFolders": 1,
      "owner": "string",
      "ownerId": "string",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletion` | date | Date de suppression du fichier. |
| `id` | number | Identifiant numérique unique de l'élément de la corbeille. |
| `isFile` | boolean | Indique s'il s'agit d'un fichier ou d'un dossier. |
| `modification` | date | Date de dernière modification du fichier avant suppression. |
| `name` | string | Nom de l'élément de la corbeille. |
| `nbFiles` | number | Nombre de fichiers présents dans le dossier. Ne s'applique pas aux fichiers |
| `nbFolders` | number | Nombre de sous-dossiers présents dans le dossier. Ne s'applique pas aux fichiers |
| `owner` | string | Nom complet de l'utilisateur propriétaire du fichier supprimé. |
| `ownerId` | string | Identifiant unique de l'utilisateur propriétaire du fichier supprimé. |
| `size` | number | Taille de l'élément de la corbeille. |

## Native endpoint

Through the native NetExplorer API, this operation is `GET /trash/:trashId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trash-by-trash-id.md) for the provider-specific parameters and requirements.

