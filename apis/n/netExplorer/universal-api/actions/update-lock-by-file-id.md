# NetExplorer: Update Lock



```
PUT https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-lock-by-file-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-lock-by-file-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-lock-by-file-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileId` | string | yes |  |

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

Through the native NetExplorer API, this operation is `PUT /lock/:fileId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lock-by-file-id.md) for the provider-specific parameters and requirements.

