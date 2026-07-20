# NetExplorer: List Delegates



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-delegates-by-group-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-delegates-by-group-id?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-delegates-by-group-id?${params}`, {
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
| `groupId` | string | yes |  |

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

Through the native NetExplorer API, this operation is `GET /delegates/:groupId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-delegates-by-group-id.md) for the provider-specific parameters and requirements.

