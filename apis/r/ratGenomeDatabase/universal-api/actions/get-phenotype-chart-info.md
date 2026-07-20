# Rat Genome Database: Get Phenotype Chart Info



```
GET https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-phenotype-chart-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rat Genome Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-phenotype-chart-info?connectionId=$CONNECTION_ID&speciesTypeKey=1&termString=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "speciesTypeKey": "1",
  "termString": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-phenotype-chart-info?${params}`, {
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
| `termString` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ageRanges": [
        {}
      ],
      "conditionSet": {},
      "measurements": [
        {}
      ],
      "methods": [
        {}
      ],
      "records": [
        {}
      ],
      "samples": [
        {}
      ],
      "termResolver": {},
      "valueRange": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ageRanges` | array<object> | Available age range buckets. |
| `conditionSet` | object | Condition set metadata. |
| `measurements` | array<object> | Referenced measurement definitions. |
| `methods` | array<object> | Measurement methods referenced by the response. |
| `records` | array<object> | Quantitative phenotype records. |
| `samples` | array<object> | Referenced sample records. |
| `termResolver` | object | Resolved ontology terms and metadata. |
| `valueRange` | object | Minimum and maximum observed values. |

## Native endpoint

Through the native Rat Genome Database API, this operation is `GET /phenotype/phenominer/chart/:speciesTypeKey/:termString` (base URL `https://rest.rgd.mcw.edu/rgdws`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-phenotype-chart-info.md) for the provider-specific parameters and requirements.

