# NetExplorer: Update Sharelink



```
PUT https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-sharelink-by-sharelink-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-sharelink-by-sharelink-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sharelinkId": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-sharelink-by-sharelink-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sharelinkId": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sharelinkId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoupdate": true,
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "files": [
        {}
      ],
      "fileType": "string",
      "id": 1,
      "isValid": true,
      "key": "string",
      "maxDownloads": 1,
      "nbDownloads": 1,
      "notify": true,
      "onlyPreview": true,
      "owner": "string",
      "ownerId": "string",
      "passwordProtected": "string",
      "remainingDownloads": 1,
      "thumbToken": "string",
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoupdate` | boolean | Indique si le partage pointe toujours vers la dernière version du fichier cible ou non. |
| `expirationDate` | date | Date d'expiration du partage. Lorsque le partage expire, le lien n'est pas supprimé mais le fichier n'est plus téléchargeable par celui-ci. |
| `files` | array<object> | Liste d'objets Fichier contenu dans le partage par lien. |
| `fileType` | string | Type de fichier. Peut valoir image ou document. Attention Ce champ n'est renseigné que si le générateur de miniatures gère ce format de fichiers. |
| `id` | number | Identifiant numérique unique du partage par lien. |
| `isValid` | boolean | Indique si le fichier est téléchargeable via ce lien ou non. |
| `key` | string | Clé de téléchargement du partage par lien. Il est possible de réutiliser la même clé pour plusieurs fichiers. Les différents fichiers seront alors listés ensemble lorsque le destinataire ouvrira le lien. |
| `maxDownloads` | number | Nombre de téléchargements maximum avant désactivation du partage. |
| `nbDownloads` | number | Nombre de téléchargements effectués sur ce partage. |
| `notify` | boolean | Notifier l'utilisateur ayant généré le partage par lien lors du téléchargement du fichier par le destinataire. |
| `onlyPreview` | boolean | Indique si le partage donne le droit uniquement à l'aperçu des fichiers. |
| `owner` | string | Nom complet de l'utilisateur ayant généré le partage par lien. |
| `ownerId` | string | Identifiant unique de l'utilisateur. |
| `passwordProtected` | string | Clé unique indiquant si le fichier est protégé par mot de passe ou non. Si la même clé est utilisée pour 2 liens différents, le mot de passe est alors le même. Vaut null si le lien est n'est pas protégé par mot de passe. |
| `remainingDownloads` | number | Nombre de téléchargements restants. |
| `thumbToken` | string | Clé de téléchargement de la miniature du fichier. A utiliser avec le générateur de miniatures rattaché à la plateforme. Attention Ce champ n'est renseigné que si le générateur de miniatures gère ce format de fichiers. |
| `type` | number | Indique si le lien est d'un certain type. ValeurApplication 1Protégé par mot de passe envoyé par sms |

## Native endpoint

Through the native NetExplorer API, this operation is `PUT /sharelink/:sharelinkId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sharelink-by-sharelink-id.md) for the provider-specific parameters and requirements.

