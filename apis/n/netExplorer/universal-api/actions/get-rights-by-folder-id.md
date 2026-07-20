# NetExplorer: List Rights



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-rights-by-folder-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-rights-by-folder-id?connectionId=$CONNECTION_ID&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-rights-by-folder-id?${params}`, {
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
      "browse": true,
      "delete": true,
      "download": true,
      "edit": true,
      "folderId": 1,
      "id": 1,
      "read": true,
      "share": true,
      "target": "string",
      "targetId": 1,
      "write": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browse` | boolean | Indique si l'utilisateur a le droit de naviguer dans le dossier. Si ce champ vaut false, l'utilisateur n'aura plus accès au dossier courant. |
| `delete` | boolean | Indique si l'utilisateur peut supprimer un fichier de ce dossier. |
| `download` | boolean | Indique si l'utilisateur peut télécharger les fichiers présents dans le dossier. |
| `edit` | boolean | Indique si l'utilisateur peur modifier un fichier existant. |
| `folderId` | number | Identifiant numérique unique du dossier. |
| `id` | number | Identifiant numérique unique du droit. |
| `read` | boolean | Indique si l'utilisateur peut voir la liste des fichiers du dossier courant, et en avoir un aperçu. |
| `share` | boolean | Indique si l'utilisateur peut inviter des participants à collaborer sur le dossier, et créer des liens de téléchargement/dépôt. |
| `target` | string | Nom complet de l'utilisateur cible. |
| `targetId` | number | Identifiant unique de l'utilisateur auquel est accordé le droit. |
| `write` | boolean | Indique si l'utilisateur peut ajouter de nouveaux fichiers. |

## Native endpoint

Through the native NetExplorer API, this operation is `GET /rights/:folderId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rights-by-folder-id.md) for the provider-specific parameters and requirements.

