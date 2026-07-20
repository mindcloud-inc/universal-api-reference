# Pappers: Get Company Map



```
GET https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-company-map
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pappers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-company-map?connectionId=$CONNECTION_ID&siren=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siren": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-company-map?${params}`, {
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
| `siren` | string | yes | French company SIREN identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entreprises": [
        {}
      ],
      "liensEntreprisesEntreprises": [
        [
          "string"
        ]
      ],
      "liensEntreprisesPersonnes": [
        [
          "string"
        ]
      ],
      "personnes": [
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
| `entreprises` | array<object> |  |
| `liensEntreprisesEntreprises` | array<array> |  |
| `liensEntreprisesPersonnes` | array<array> |  |
| `personnes` | array<object> |  |

## Native endpoint

Through the native Pappers API, this operation is `GET /entreprise/cartographie` (base URL `https://api.pappers.fr/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-map.md) for the provider-specific parameters and requirements.

