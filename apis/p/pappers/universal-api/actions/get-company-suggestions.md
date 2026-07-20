# Pappers: Get Company Suggestions



```
GET https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-company-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pappers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-company-suggestions?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-company-suggestions?${params}`, {
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
      "anneeEffectif": 1,
      "anneeFinances": 1,
      "association": {},
      "capital": 1,
      "categorieJuridique": "string",
      "chiffreAffaires": 1,
      "codeNaf": "string",
      "conventionsCollectives": [
        {}
      ],
      "dateCessation": "string",
      "dateCreation": "string",
      "dateCreationFormate": "string",
      "denomination": "string",
      "diffusable": true,
      "domaineActivite": "string",
      "economieSocialeEtSolidaire": true,
      "effectif": "string",
      "effectifMax": 1,
      "effectifMin": 1,
      "effectifsFinances": 1,
      "entrepriseCessee": 1,
      "entrepriseEmployeuse": 1,
      "formeJuridique": "string",
      "libelleCodeNaf": "string",
      "nom": "string",
      "nomEntreprise": "string",
      "personneMorale": true,
      "prenom": "string",
      "resultat": 1,
      "sexe": "string",
      "siege": {},
      "siren": "string",
      "sirenFormate": "string",
      "statutConsolide": "string",
      "statutRcs": "string",
      "trancheEffectif": "string",
      "villes": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `anneeEffectif` | number |  |
| `anneeFinances` | number |  |
| `association` | object |  |
| `capital` | number |  |
| `categorieJuridique` | string |  |
| `chiffreAffaires` | number |  |
| `codeNaf` | string |  |
| `conventionsCollectives` | array<object> |  |
| `dateCessation` | string |  |
| `dateCreation` | string |  |
| `dateCreationFormate` | string |  |
| `denomination` | string |  |
| `diffusable` | boolean |  |
| `domaineActivite` | string |  |
| `economieSocialeEtSolidaire` | boolean |  |
| `effectif` | string |  |
| `effectifMax` | number |  |
| `effectifMin` | number |  |
| `effectifsFinances` | number |  |
| `entrepriseCessee` | number |  |
| `entrepriseEmployeuse` | number |  |
| `formeJuridique` | string |  |
| `libelleCodeNaf` | string |  |
| `nom` | string |  |
| `nomEntreprise` | string |  |
| `personneMorale` | boolean |  |
| `prenom` | string |  |
| `resultat` | number |  |
| `sexe` | string |  |
| `siege` | object |  |
| `siren` | string |  |
| `sirenFormate` | string |  |
| `statutConsolide` | string |  |
| `statutRcs` | string |  |
| `trancheEffectif` | string |  |
| `villes` | array<string> |  |

## Native endpoint

Through the native Pappers API, this operation is `GET /suggestions` (base URL `https://api.pappers.fr/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-suggestions.md) for the provider-specific parameters and requirements.

