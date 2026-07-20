# Rat Genome Database: Get Genes In Region



```
GET https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-genes-in-region
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rat Genome Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-genes-in-region?connectionId=$CONNECTION_ID&chr=string&start=1&stop=1&mapKey=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chr": "string",
  "start": "1",
  "stop": "1",
  "mapKey": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-genes-in-region?${params}`, {
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
| `chr` | string | yes |  |
| `start` | number | yes |  |
| `stop` | number | yes |  |
| `mapKey` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chromosome": "string",
      "mapKey": 1,
      "rgdId": 1,
      "start": 1,
      "stop": 1,
      "strand": "string",
      "symbol": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chromosome` | string | Chromosome label. |
| `mapKey` | number | Assembly map key. |
| `rgdId` | number | RGD identifier for the gene. |
| `start` | number | Genomic start position. |
| `stop` | number | Genomic stop position. |
| `strand` | string | Genomic strand. |
| `symbol` | string | Gene symbol. |

## Native endpoint

Through the native Rat Genome Database API, this operation is `GET /genes/region/:chr/:start/:stop/:mapKey` (base URL `https://rest.rgd.mcw.edu/rgdws`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-genes-in-region.md) for the provider-specific parameters and requirements.

