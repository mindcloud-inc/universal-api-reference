# Zillow Econ: Get region metadata

Retrieves region metadata from Zillow Econ.

```
GET https://connect.mindcloud.co/v1/universal/zillowEcon/latest/actions/get-region-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zillow Econ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowEcon/latest/actions/get-region-metadata?connectionId=$CONNECTION_ID&stateCodeFIPS=48" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stateCodeFIPS": "48"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zillowEcon/latest/actions/get-region-metadata?${params}`, {
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
| `stateCodeFIPS` | string | yes | Two-digit state FIPS code for the region metadata lookup. Default: `48`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "municipalCodeFIPS": "string",
      "region": "string",
      "regionCity": "string",
      "regionCounty": "string",
      "regionID": 1,
      "regionMetro": "string",
      "regionState": "string",
      "stateCodeFIPS": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `municipalCodeFIPS` | string | Three-digit FIPS municipal code. |
| `region` | string | Region name. |
| `regionCity` | string | City containing the region. |
| `regionCounty` | string | County containing the region. |
| `regionID` | number | Primary identifier for the region. |
| `regionMetro` | string | Metro area containing the region. |
| `regionState` | string | State abbreviation containing the region. |
| `stateCodeFIPS` | string | Two-digit FIPS state code. |

## Native endpoint

Through the native Zillow Econ API, this operation is `GET /zgecon/region` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-region-metadata.md) for the provider-specific parameters and requirements.

