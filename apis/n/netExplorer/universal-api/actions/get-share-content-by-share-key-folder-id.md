# NetExplorer: Get Share Content



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-share-content-by-share-key-folder-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-share-content-by-share-key-folder-id?connectionId=$CONNECTION_ID&shareKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shareKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-share-content-by-share-key-folder-id?${params}`, {
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
| `shareKey` | string | yes |  |
| `folderId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entityType": 1,
      "guid": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entityType` | number | Type d'entité ValeurType associé 0Dossier |
| `guid` | string | Le guid du fichier (Si l'entité est un fichier) |
| `id` | number | L'identifiant unique de l'entité |

## Native endpoint

Through the native NetExplorer API, this operation is `GET /share/content/:shareKey/[:folderId]` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-share-content-by-share-key-folder-id.md) for the provider-specific parameters and requirements.

