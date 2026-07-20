# Rat Genome Database: Get Variant By RS ID



```
GET https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-variant-by-rs-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rat Genome Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-variant-by-rs-id?connectionId=$CONNECTION_ID&rsId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rsId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-variant-by-rs-id?${params}`, {
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
| `rsId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chromosome": "string",
      "clinvarId": "string",
      "endPos": 1,
      "genicStatus": "string",
      "id": 1,
      "mapKey": 1,
      "paddingBase": "string",
      "referenceNucleotide": "string",
      "rsId": "string",
      "speciesTypeKey": 1,
      "startPos": 1,
      "variantNucleotide": "string",
      "variantType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chromosome` | string | Chromosome label. |
| `clinvarId` | string | ClinVar identifier when available. |
| `endPos` | number | Variant end position. |
| `genicStatus` | string | Genic status label. |
| `id` | number | Variant record identifier. |
| `mapKey` | number | Assembly map key. |
| `paddingBase` | string | Padding base for indels when available. |
| `referenceNucleotide` | string | Reference nucleotide sequence. |
| `rsId` | string | dbSNP rsID when available. |
| `speciesTypeKey` | number | Species type key. |
| `startPos` | number | Variant start position. |
| `variantNucleotide` | string | Alternate nucleotide sequence. |
| `variantType` | string | Variant type label. |

## Native endpoint

Through the native Rat Genome Database API, this operation is `GET /variants/:rsId` (base URL `https://rest.rgd.mcw.edu/rgdws`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-variant-by-rs-id.md) for the provider-specific parameters and requirements.

