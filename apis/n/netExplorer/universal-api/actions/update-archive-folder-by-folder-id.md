# NetExplorer: Update Folder



```
PUT https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-archive-folder-by-folder-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-archive-folder-by-folder-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-archive-folder-by-folder-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canAdminAlerts": true,
      "canAdminRights": true,
      "canDelete": true,
      "canDlink": true,
      "canDownload": true,
      "canEdit": true,
      "canRead": true,
      "canShare": true,
      "canUlink": true,
      "canWrite": true,
      "content": "string",
      "creation": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "modification": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "nbAnnotations": 1,
      "nbDFiles": 1,
      "nbDFolders": 1,
      "nbFiles": 1,
      "nbFolders": 1,
      "nbParticipants": 1,
      "nbUnreadAnnotations": 1,
      "owner": "string",
      "ownerId": "string",
      "parentId": 1,
      "path": "string",
      "pathName": "Ava Chen",
      "purgeFrequency": 1,
      "quota": 1,
      "selfAlert": true,
      "shared": true,
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canAdminAlerts` | boolean | Indique si l'utilisateur courant peut gérer les alertes emails sur le dossier. |
| `canAdminRights` | boolean | Indique si l'utilisateur courant peut gérer les droits sur le dossier. |
| `canDelete` | boolean | Indique si l'utilisateur courant peut supprimer des documents présents dans ce dossier. |
| `canDlink` | boolean | Indique si l'utilisateur peut générer un lien de téléchargement sur ce dossier, en prenant en compte les droits d'accès et les informations de configuration de la plateforme. |
| `canDownload` | boolean | Indique si l'utilisateur courant peut télécharger des documents présents dans ce dossier. |
| `canEdit` | boolean | Indique si l'utilisateur courant peut modifier des documents présents dans ce dossier. |
| `canRead` | boolean | Indique si l'utilisateur courant peut avoir un aperçu des documents présents dans ce dossier. |
| `canShare` | boolean | Indique si l'utilisateur courant peut partager des documents présents dans ce dossier avec des personnes extérieures. |
| `canUlink` | boolean | Indique si l'utilisateur peut générer un lien de dépôt sur ce dossier, en prenant en compte les droits d'accès et les informations de configuration de la plateforme. |
| `canWrite` | boolean | Indique si l'utilisateur courant peut créer de nouveaux fichiers dans ce dossier. |
| `content` | string | Contient 2 entrées, "files" et "folders", contenant les listes de fichiers et dossiers contenu dans le dossier courant. Ne sera retourné que si le listing récursif est demandé et que le niveau de profondeur indiqué n'a pas été atteint.{ "files": [ // Objets Fichier { "id": 1, "name": [ ... ] }, ... ], "folders": [ // Objets Dossier { "id": 1, "name": [ ... ] }, ... ] } |
| `creation` | date | Date de création du dossier. |
| `id` | number | Identifiant numérique unique du dossier. |
| `modification` | date | Date de dernière modification du contenu du dossier. |
| `name` | string | Nom du dossier. |
| `nbAnnotations` | number | Nombre d'annotations sur le dossier. Valeur présente uniquement si > 0. |
| `nbDFiles` | number | Nombre de fichiers présents, sans prendre en compte toute l'arborescence inférieure. |
| `nbDFolders` | number | Nombre de sous-dossiers présents, sans prendre en compte toute l'arborescence inférieure. |
| `nbFiles` | number | Nombre total de fichiers (totalité de l'arborescence). |
| `nbFolders` | number | Nombre total de sous-dossiers (totalité de l'arborescence). |
| `nbParticipants` | number | Nombre de participants invités sur le dossier. Valeur présente uniquement si > 0. |
| `nbUnreadAnnotations` | number | Nombre d'annotations non-lues sur le dossier. Valeur présente uniquement si > 0. |
| `owner` | string | Nom complet de l'utilisateur propriétaire du dossier. |
| `ownerId` | string | Identifiant unique de l'utilisateur propriétaire du dossier. |
| `parentId` | number | Identifiant numérique unique du dossier parent. |
| `path` | string | Chemin d'accès au dossier, composé des identifiants uniques des dossiers parents. |
| `pathName` | string | Chemin d'accès au dossier, composé des noms des dossiers parents, limité par les droits d'accès de l'utilisateur. |
| `purgeFrequency` | number | Délai après lequel les fichiers sont automatiquement supprimés du dossier. 0 = désactivé, sinon un nombre de jours |
| `quota` | number | Quota d'espace disque appliqué au dossier. 0 = illimité, -1 = Hériter du dossier parent, sinon un nombre d'octets. |
| `selfAlert` | boolean | Indique si l'utilisateur courant est alerté des modifications sur le dossier. Si l'option self_alert de la configuration n'est pas activée, ce champ sera totalement absent des réponses. |
| `shared` | boolean | Indique si le dossier est un dossier d'un espace privé qui a été partagé. |
| `size` | number | Taille en octets du dossier. |

## Native endpoint

Through the native NetExplorer API, this operation is `PUT /archive/folder/:folderId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-archive-folder-by-folder-id.md) for the provider-specific parameters and requirements.

