# NetExplorer: Get Portal Root



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-root-portal-by-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-root-portal-by-filter?connectionId=$CONNECTION_ID&filter=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filter": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-root-portal-by-filter?${params}`, {
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
| `filter` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {},
      "id": 1,
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | object | Contenu de la racine. |
| `id` | number | Identifiant de la racine. |
| `name` | string | Nom de la racine. |
| `type` | string | Type de racine. |

## Native endpoint

Through the native NetExplorer API, this operation is `GET /root/portal/:filter` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-root-portal-by-filter.md) for the provider-specific parameters and requirements.

