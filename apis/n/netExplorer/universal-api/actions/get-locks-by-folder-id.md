# NetExplorer: List Locks



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-locks-by-folder-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-locks-by-folder-id?connectionId=$CONNECTION_ID&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-locks-by-folder-id?${params}`, {
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
      "date": "2026-05-07T12:00:00.000Z",
      "file": "string",
      "locked": true,
      "owner": "string",
      "ownerId": "string",
      "writeable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Date à laquelle le verrouillage a été créé. |
| `file` | string | Identifiant global unique du fichier (GUID) auquel ce verrou est rattaché. |
| `locked` | boolean | Indique si le fichier est actuellement verrouillé, quelque soit l'utilisateur l'ayant verrouillé. |
| `owner` | string | Nom complet du propriétaire du verrou. |
| `ownerId` | string | Identifiant unique du propriétaire du verrou. |
| `writeable` | boolean | Indique si le fichier est accessible en écriture. Peut être à true même si locked = true, notamment si le fichier est verrouillé par l'utilisateur courant. |

## Native endpoint

Through the native NetExplorer API, this operation is `GET /locks/:folderId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-locks-by-folder-id.md) for the provider-specific parameters and requirements.

