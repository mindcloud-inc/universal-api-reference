# Rat Genome Database: Get Genes By Species



```
GET https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-genes-by-species
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rat Genome Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-genes-by-species?connectionId=$CONNECTION_ID&speciesTypeKey=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "speciesTypeKey": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-genes-by-species?${params}`, {
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
| `speciesTypeKey` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agrDescription": "string",
      "description": "string",
      "ensemblFullName": "Ava Chen",
      "ensemblGeneSymbol": "string",
      "ensemblGeneType": "string",
      "geneSource": "string",
      "key": 1,
      "mergedDescription": "string",
      "name": "Ava Chen",
      "ncbiAnnotStatus": "string",
      "nomenReviewDate": "2026-05-07T12:00:00.000Z",
      "nomenSource": "string",
      "notes": "string",
      "refSeqStatus": "string",
      "rgdId": 1,
      "soAccId": "string",
      "speciesTypeKey": 1,
      "symbol": "string",
      "taglessAlleleSymbol": "string",
      "type": "string",
      "variant": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agrDescription` | string | Alliance of Genome Resources description. |
| `description` | string | Gene description. |
| `ensemblFullName` | string | Ensembl full gene name. |
| `ensemblGeneSymbol` | string | Ensembl gene symbol. |
| `ensemblGeneType` | string | Ensembl gene type. |
| `geneSource` | string | Primary source for the gene record. |
| `key` | number | Internal gene key. |
| `mergedDescription` | string | Merged long-form description. |
| `name` | string | Gene name. |
| `ncbiAnnotStatus` | string | NCBI annotation status when available. |
| `nomenReviewDate` | date | Nomenclature review timestamp. |
| `nomenSource` | string | Nomenclature source when available. |
| `notes` | string | Additional provider notes. |
| `refSeqStatus` | string | RefSeq status. |
| `rgdId` | number | RGD identifier for the gene. |
| `soAccId` | string | Sequence Ontology accession. |
| `speciesTypeKey` | number | Species type key. |
| `symbol` | string | Gene symbol. |
| `taglessAlleleSymbol` | string | Tagless allele symbol when available. |
| `type` | string | Gene type label. |
| `variant` | boolean | Whether the record represents a variant. |

## Native endpoint

Through the native Rat Genome Database API, this operation is `GET /genes/species/:speciesTypeKey` (base URL `https://rest.rgd.mcw.edu/rgdws`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-genes-by-species.md) for the provider-specific parameters and requirements.

