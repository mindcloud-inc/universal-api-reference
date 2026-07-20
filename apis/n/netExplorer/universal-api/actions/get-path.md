# NetExplorer: Get Path



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-path
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-path?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-path?${params}`, {
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
      "canDelete": true,
      "canDownload": true,
      "canEdit": true,
      "canShare": true,
      "canWrite": true,
      "creation": "2026-05-07T12:00:00.000Z",
      "downloadToken": "string",
      "fileType": "string",
      "guid": "string",
      "hash": "string",
      "id": 1,
      "lock": "string",
      "meta": "string",
      "modification": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "nbAnnotations": 1,
      "nbUnreadAnnotations": 1,
      "nbVersions": 1,
      "owner": "string",
      "ownerId": "string",
      "parentId": 1,
      "path": "string",
      "thumbToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canDelete` | boolean | Indique si l'utilisateur courant peut supprimer le fichier. |
| `canDownload` | boolean | Indique si l'utilisateur courant peut télécharger le fichier. |
| `canEdit` | boolean | Indique si l'utilisateur courant peut modifier une version existante du fichier. |
| `canShare` | boolean | Indique si l'utilisateur courant peut partager le fichier vers l'exterieur. |
| `canWrite` | boolean | Indique si l'utilisateur courant peut créer de nouvelles versions du fichier. |
| `creation` | date | Date de création de la version courante du fichier. |
| `downloadToken` | string | Token d'accès pour le téléchargement du fichier. |
| `fileType` | string | Type d'aperçu du fichier. Peut valoir image, document ou video si l'aperçu est disponible pour ce fichier. |
| `guid` | string | Identifiant global unique du fichier (GUID) du fichier. |
| `hash` | string | Hash MD5 du fichier. |
| `id` | number | Identifiant numérique unique du fichier (version). |
| `lock` | string | Contient les informations sur le verrou actuellement en place, s'il y en a un. Sinon, vaut null. |
| `meta` | string | Contient des méta-données. Le tableau a le format suivant: { "author": "Luc MARCHAND", // Auteur du document "creator": "LibreOffice", // Logiciel de traitement de texte utilisé "date": "Sun Sep 1 00:00:00 2013", // Date de dernière édition du document "keywords": "mots clés document", // Mots clés "pages": 10, // Nombre de pages "producer": "GhostScript", // Logiciel ayant produit le fichier "subject": "Détail des ventes pour l'année 2013", // Sujet détaillé du document "title": "Rapport ventes 2013" // Titre du document } |
| `modification` | date | Date de dernière modification de la version la plus récente du fichier. |
| `name` | string | Nom du fichier. |
| `nbAnnotations` | number | Nombre d'annotations sur le fichier. Valeur présente uniquement si > 0. |
| `nbUnreadAnnotations` | number | Nombre d'annotations non-lues sur le fichier. Valeur présente uniquement si > 0 |
| `nbVersions` | number | Nombre de versions existantes pour ce fichier. Valeur présente uniquement si > 1. |
| `owner` | string | Nom complet de l'utilisateur propriétaire du fichier. |
| `ownerId` | string | Identifiant unique de l'utilisateur propriétaire du fichier. |
| `parentId` | number | Identifiant numérique unique du dossier parent. |
| `path` | string | Chemin d'accès au fichier, composé des identifiants uniques des dossiers parents. |
| `thumbToken` | string | Token d'accès aux miniatures de ce fichier si le format est supporté. |

## Native endpoint

Through the native NetExplorer API, this operation is `GET /path` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-path.md) for the provider-specific parameters and requirements.

