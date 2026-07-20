# Rat Genome Database: Get Chromosomes By Primary Assembly



```
GET https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-chromosomes-by-primary-assembly
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rat Genome Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-chromosomes-by-primary-assembly?connectionId=$CONNECTION_ID&speciesTypeKey=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "speciesTypeKey": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/get-chromosomes-by-primary-assembly?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Chromosome label. |

## Native endpoint

Through the native Rat Genome Database API, this operation is `GET /maps/chrForSpecies/:speciesTypeKey` (base URL `https://rest.rgd.mcw.edu/rgdws`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chromosomes-by-primary-assembly.md) for the provider-specific parameters and requirements.

