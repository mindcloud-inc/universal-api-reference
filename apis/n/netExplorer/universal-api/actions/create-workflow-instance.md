# NetExplorer: Create Instance



```
POST https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-workflow-instance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-workflow-instance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-workflow-instance', {
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
      "creation": "string",
      "dataObjects": [
        {}
      ],
      "flux": "string",
      "id": 1,
      "isClosed": true,
      "objectId": 1,
      "objectType": "string",
      "ownerId": 1,
      "properties": "string",
      "state": "string",
      "transitionsAvailable": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creation` | string | Date de création du flux |
| `dataObjects` | array<object> | Tableau d'objets rattachés au flux |
| `flux` | string | Clé de traduction du nom du flux. |
| `id` | number | Identifiant de l'instance du flux. |
| `isClosed` | boolean | Informe si l'instance du flux est dans un état ne pouvant évoluer vers un autre état. |
| `objectId` | number | Identifiant de l'objet sur lequel l'instance du flux est rattaché. |
| `objectType` | string | Type d'objet sur lequel l'instance du flux est rattaché. |
| `ownerId` | number | Identifiant du créateur de l'instance du flux. |
| `properties` | string | Tableau json des propriétés du flux. |
| `state` | string | Objet contenu l'identifiant et le nom de l'état du flux. |
| `transitionsAvailable` | array<object> | Tableau listant les transitions disponible pour l'état actuel de l'instance du flux. |

## Native endpoint

Through the native NetExplorer API, this operation is `POST /workflow/instance` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workflow-instance.md) for the provider-specific parameters and requirements.

