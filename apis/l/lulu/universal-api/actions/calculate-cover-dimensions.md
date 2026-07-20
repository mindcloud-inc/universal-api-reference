# Lulu: Calculate Cover Dimensions

Calculates cover dimensions in Lulu.

```
GET https://connect.mindcloud.co/v1/universal/lulu/latest/actions/calculate-cover-dimensions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lulu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/calculate-cover-dimensions?connectionId=$CONNECTION_ID&interiorPageCount=32&podPackageId=0600X0900.BW.STD.PB.060UW444.MXX" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "interiorPageCount": "32",
  "podPackageId": "0600X0900.BW.STD.PB.060UW444.MXX"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lulu/latest/actions/calculate-cover-dimensions?${params}`, {
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
| `interiorPageCount` | number | yes | Interior page count for Lulu cover dimensions. Default: `32`. |
| `podPackageId` | string | yes | Lulu pod package ID for cover dimensions. Default: `0600X0900.BW.STD.PB.060UW444.MXX`. |
| `unit` | string | no | Output unit for Lulu cover dimensions. Default: `in`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "height": "string",
      "unit": "string",
      "width": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `height` | string |  |
| `unit` | string |  |
| `width` | string |  |

## Native endpoint

Through the native Lulu API, this operation is `POST /cover-dimensions/` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-cover-dimensions.md) for the provider-specific parameters and requirements.

