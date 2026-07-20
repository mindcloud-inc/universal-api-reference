# Rat Genome Database: Get Strains By Search Term



```
GET https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-strains-by-search-term
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rat Genome Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-strains-by-search-term?connectionId=$CONNECTION_ID&term=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "term": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-strains-by-search-term?${params}`, {
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
| `term` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "diseaseOrPhenotypeTerm": "string",
      "evidence": "string",
      "qualifier": "string",
      "refRgdId": "string",
      "strain": "string",
      "strainRgdId": 1,
      "strainType": "string",
      "withConditionsTerm": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `diseaseOrPhenotypeTerm` | string | Matched disease or phenotype term. |
| `evidence` | string | Evidence code. |
| `qualifier` | string | Qualifier for the disease or phenotype association. |
| `refRgdId` | string | Reference RGD identifier. |
| `strain` | string | Strain symbol or display label. |
| `strainRgdId` | number | RGD identifier for the strain. |
| `strainType` | string | Strain type label. |
| `withConditionsTerm` | string | Associated condition term when available. |

## Native endpoint

Through the native Rat Genome Database API, this operation is `GET /strains/search/:term` (base URL `https://rest.rgd.mcw.edu/rgdws`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-strains-by-search-term.md) for the provider-specific parameters and requirements.

