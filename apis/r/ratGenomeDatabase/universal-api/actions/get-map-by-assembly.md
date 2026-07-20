# Rat Genome Database: Get Map By Assembly



```
GET https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-map-by-assembly
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rat Genome Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-map-by-assembly?connectionId=$CONNECTION_ID&mapKey=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mapKey": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-map-by-assembly?${params}`, {
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
| `mapKey` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dbsnpVersion": "string",
      "description": "string",
      "key": 1,
      "methodKey": 1,
      "name": "Ava Chen",
      "notes": "string",
      "primaryRefAssembly": true,
      "rank": 1,
      "refSeqAssemblyAcc": "string",
      "refSeqAssemblyName": "Ava Chen",
      "rgdId": 1,
      "source": "string",
      "speciesTypeKey": 1,
      "ucscAssemblyId": "string",
      "unit": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dbsnpVersion` | string | dbSNP version when available. |
| `description` | string | Human-readable map description. |
| `key` | number | Map key identifier. |
| `methodKey` | number | Method key for the map entry. |
| `name` | string | Map or assembly name. |
| `notes` | string | Provider notes for the map. |
| `primaryRefAssembly` | boolean | Whether this is the primary reference assembly. |
| `rank` | number | Ordering rank from RGD. |
| `refSeqAssemblyAcc` | string | RefSeq assembly accession. |
| `refSeqAssemblyName` | string | RefSeq assembly name. |
| `rgdId` | number | RGD identifier for the map. |
| `source` | string | Source database for the map. |
| `speciesTypeKey` | number | Species type key. |
| `ucscAssemblyId` | string | UCSC assembly identifier when available. |
| `unit` | string | Coordinate unit. |
| `version` | string | Map version when available. |

## Native endpoint

Through the native Rat Genome Database API, this operation is `GET /maps/assembly/:mapKey` (base URL `https://rest.rgd.mcw.edu/rgdws`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-map-by-assembly.md) for the provider-specific parameters and requirements.

