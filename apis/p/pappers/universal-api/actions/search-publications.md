# Pappers: Search Publications



```
GET https://connect.mindcloud.co/v1/universal/pappers/latest/actions/search-publications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pappers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pappers/latest/actions/search-publications?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pappers/latest/actions/search-publications?${params}`, {
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
| `q` | string | yes | Search term |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contenu": "string",
      "date": "string",
      "entreprise": {},
      "siren": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contenu` | string |  |
| `date` | string |  |
| `entreprise` | object |  |
| `siren` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Pappers API, this operation is `GET /recherche-publications` (base URL `https://api.pappers.fr/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-publications.md) for the provider-specific parameters and requirements.

