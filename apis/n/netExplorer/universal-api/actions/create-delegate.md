# NetExplorer: Create Delegate



```
POST https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-delegate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-delegate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/create-delegate', {
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
      "content": "string",
      "id": 1,
      "object": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Contenu de l'email. Texte ou HTML accepté. |
| `id` | number | Identifiant numérique unique de l'email. |
| `object` | string | Objet de l'email. |
| `type` | string | Enumération pouvant prendre les valeurs suivantes: ValeurUtilisation EM_TE_DEFAUTUtilisation interne Email par défaut de NetExplorer. |

## Native endpoint

Through the native NetExplorer API, this operation is `POST /delegate` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-delegate.md) for the provider-specific parameters and requirements.

