# Pappers: Search Companies



```
GET https://connect.mindcloud.co/v1/universal/pappers/latest/actions/search-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pappers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pappers/latest/actions/search-companies?connectionId=$CONNECTION_ID&q=ACME" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "ACME"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pappers/latest/actions/search-companies?${params}`, {
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
| `q` | string | yes | Search query. Example: `ACME`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "anneeEffectif": 1,
      "anneeFinances": 1,
      "association": {},
      "beneficiaires": [
        {}
      ],
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
      "dirigeants": [
        {}
      ],
      "documents": [
        {}
      ],
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
      "nbBeneficiairesTotal": 1,
      "nbDirigeantsTotal": 1,
      "nbDocumentsAvecMentions": 1,
      "nbDocumentsTotal": 1,
      "nbPublicationsAvecMentions": 1,
      "nbPublicationsTotal": 1,
      "nom": "string",
      "nomEntreprise": "string",
      "personneMorale": true,
      "prenom": "string",
      "publications": [
        {}
      ],
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
| `beneficiaires` | array<object> |  |
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
| `dirigeants` | array<object> |  |
| `documents` | array<object> |  |
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
| `nbBeneficiairesTotal` | number |  |
| `nbDirigeantsTotal` | number |  |
| `nbDocumentsAvecMentions` | number |  |
| `nbDocumentsTotal` | number |  |
| `nbPublicationsAvecMentions` | number |  |
| `nbPublicationsTotal` | number |  |
| `nom` | string |  |
| `nomEntreprise` | string |  |
| `personneMorale` | boolean |  |
| `prenom` | string |  |
| `publications` | array<object> |  |
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

Through the native Pappers API, this operation is `GET /recherche` (base URL `https://api.pappers.fr/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-companies.md) for the provider-specific parameters and requirements.

