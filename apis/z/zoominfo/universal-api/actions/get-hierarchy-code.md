# Zoominfo: Get Hierarchy Code

Retrieves hierarchy codes from ZoomInfo.

```
GET https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/get-hierarchy-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoominfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/get-hierarchy-code?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/get-hierarchy-code?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "combinations": {
        "DPSUHQ": "string",
        "DPSUHQFE": "string",
        "DPSUHQFR": "string",
        "DPSUIL": "string",
        "DPSUILFE": "string",
        "GPDPSUHQ": "string",
        "GPDPSUHQFE": "string",
        "GPDPSUHQFR": "string",
        "GPHQ": "string",
        "GPHQFE": "string",
        "GPHQFR": "string",
        "HQ": "string",
        "HQFE": "string",
        "HQFR": "string",
        "IL": "string",
        "ILFE": "string",
        "SUHQ": "string"
      },
      "hierachyCodes": {
        "DP": "string",
        "FE": "string",
        "FR": "string",
        "GP": "string",
        "HQ": "string",
        "IL": "string",
        "SU": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `combinations.DPSUHQ` | string |  |
| `combinations.DPSUHQFE` | string |  |
| `combinations.DPSUHQFR` | string |  |
| `combinations.DPSUIL` | string |  |
| `combinations.DPSUILFE` | string |  |
| `combinations.GPDPSUHQ` | string |  |
| `combinations.GPDPSUHQFE` | string |  |
| `combinations.GPDPSUHQFR` | string |  |
| `combinations.GPHQ` | string |  |
| `combinations.GPHQFE` | string |  |
| `combinations.GPHQFR` | string |  |
| `combinations.HQ` | string |  |
| `combinations.HQFE` | string |  |
| `combinations.HQFR` | string |  |
| `combinations.IL` | string |  |
| `combinations.ILFE` | string |  |
| `combinations.SUHQ` | string |  |
| `hierachyCodes.DP` | string |  |
| `hierachyCodes.FE` | string |  |
| `hierachyCodes.FR` | string |  |
| `hierachyCodes.GP` | string |  |
| `hierachyCodes.HQ` | string |  |
| `hierachyCodes.IL` | string |  |
| `hierachyCodes.SU` | string |  |

## Native endpoint

Through the native Zoominfo API, this operation is `GET lookup/hierarchy-code` (base URL `https://api.zoominfo.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hierarchy-code.md) for the provider-specific parameters and requirements.

