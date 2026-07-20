# Pappers: Search Directors



```
GET https://connect.mindcloud.co/v1/universal/pappers/latest/actions/search-directors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pappers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pappers/latest/actions/search-directors?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pappers/latest/actions/search-directors?${params}`, {
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
      "actuel": true,
      "datePremierePriseDePoste": "string",
      "datePriseDePoste": "string",
      "denomination": "string",
      "email": "ava@example.com",
      "entreprises": [
        {}
      ],
      "formeJuridique": "string",
      "nbEntreprisesTotal": 1,
      "nomComplet": "string",
      "personneMorale": true,
      "precedentsPostes": [
        {}
      ],
      "qualite": "string",
      "qualites": [
        "string"
      ],
      "siren": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actuel` | boolean |  |
| `datePremierePriseDePoste` | string |  |
| `datePriseDePoste` | string |  |
| `denomination` | string |  |
| `email` | string |  |
| `entreprises` | array<object> |  |
| `formeJuridique` | string |  |
| `nbEntreprisesTotal` | number |  |
| `nomComplet` | string |  |
| `personneMorale` | boolean |  |
| `precedentsPostes` | array<object> |  |
| `qualite` | string |  |
| `qualites` | array<string> |  |
| `siren` | string |  |

## Native endpoint

Through the native Pappers API, this operation is `GET /recherche-dirigeants` (base URL `https://api.pappers.fr/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-directors.md) for the provider-specific parameters and requirements.

