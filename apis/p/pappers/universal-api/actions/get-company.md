# Pappers: Get Company



```
GET https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pappers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-company?connectionId=$CONNECTION_ID&siren=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siren": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-company?${params}`, {
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
| `siren` | string | yes | French company SIREN identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "association": {},
      "beneficiaires": [
        {}
      ],
      "capital": 1,
      "chiffreAffaires": 1,
      "codeNaf": "string",
      "conventionsCollectives": [
        {}
      ],
      "dateCreation": "string",
      "denomination": "string",
      "derniersStatuts": {},
      "diffusable": true,
      "dirigeants": [
        {}
      ],
      "documents": [
        {}
      ],
      "domaineActivite": "string",
      "effectif": "string",
      "etablissements": [
        {}
      ],
      "extraitImmatriculation": {},
      "formeJuridique": "string",
      "libelleCodeNaf": "string",
      "nomEntreprise": "string",
      "personneMorale": true,
      "publications": [
        {}
      ],
      "resultat": 1,
      "siege": {},
      "siren": "string",
      "sirenFormate": "string",
      "statutConsolide": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `association` | object |  |
| `beneficiaires` | array<object> |  |
| `capital` | number |  |
| `chiffreAffaires` | number |  |
| `codeNaf` | string |  |
| `conventionsCollectives` | array<object> |  |
| `dateCreation` | string |  |
| `denomination` | string |  |
| `derniersStatuts` | object |  |
| `diffusable` | boolean |  |
| `dirigeants` | array<object> |  |
| `documents` | array<object> |  |
| `domaineActivite` | string |  |
| `effectif` | string |  |
| `etablissements` | array<object> |  |
| `extraitImmatriculation` | object |  |
| `formeJuridique` | string |  |
| `libelleCodeNaf` | string |  |
| `nomEntreprise` | string |  |
| `personneMorale` | boolean |  |
| `publications` | array<object> |  |
| `resultat` | number |  |
| `siege` | object |  |
| `siren` | string |  |
| `sirenFormate` | string |  |
| `statutConsolide` | string |  |

## Native endpoint

Through the native Pappers API, this operation is `GET /entreprise` (base URL `https://api.pappers.fr/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

