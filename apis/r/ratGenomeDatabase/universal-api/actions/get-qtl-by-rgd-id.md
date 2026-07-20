# Rat Genome Database: Get QTL By RGD ID



```
GET https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-qtl-by-rgd-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rat Genome Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-qtl-by-rgd-id?connectionId=$CONNECTION_ID&rgdId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rgdId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-qtl-by-rgd-id?${params}`, {
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
| `rgdId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chromosome": "string",
      "flank1RgdId": 1,
      "flank2RgdId": 1,
      "inheritanceType": "string",
      "key": 1,
      "linkageImage": "https://example.com",
      "lod": 1,
      "lodImage": "string",
      "mostSignificantCmoTerm": "string",
      "name": "Ava Chen",
      "notes": "string",
      "peakOffset": 1,
      "peakRgdId": 1,
      "peakRsId": "string",
      "pvalue": 1,
      "pValueMlog": 1,
      "rgdId": 1,
      "sourceUrl": "https://example.com",
      "speciesTypeKey": 1,
      "symbol": "string",
      "variance": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chromosome` | string | Chromosome label. |
| `flank1RgdId` | number | First flanking marker RGD ID when available. |
| `flank2RgdId` | number | Second flanking marker RGD ID when available. |
| `inheritanceType` | string | Inheritance type when available. |
| `key` | number | Internal QTL key. |
| `linkageImage` | string | Linkage image URL when available. |
| `lod` | number | LOD score when available. |
| `lodImage` | string | LOD image URL when available. |
| `mostSignificantCmoTerm` | string | Most significant CMO term when available. |
| `name` | string | QTL name. |
| `notes` | string | Additional provider notes. |
| `peakOffset` | number | Peak offset when available. |
| `peakRgdId` | number | Peak marker RGD ID when available. |
| `peakRsId` | string | Peak rsID when available. |
| `pvalue` | number | Reported p-value. |
| `pValueMlog` | number | Negative log p-value when available. |
| `rgdId` | number | RGD identifier for the QTL. |
| `sourceUrl` | string | Source URL when available. |
| `speciesTypeKey` | number | Species type key. |
| `symbol` | string | QTL symbol. |
| `variance` | number | Variance explained by the QTL. |

## Native endpoint

Through the native Rat Genome Database API, this operation is `GET /qtls/:rgdId` (base URL `https://rest.rgd.mcw.edu/rgdws`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-qtl-by-rgd-id.md) for the provider-specific parameters and requirements.

