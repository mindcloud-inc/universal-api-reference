# NCEI Climate Data: Get Data Type

Retrieves data type details from NCEI Climate Data.

```
GET https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/get-data-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NCEI Climate Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/get-data-type?connectionId=$CONNECTION_ID&dataTypeId=TAVG" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataTypeId": "TAVG"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nCEIClimateData/latest/actions/get-data-type?${params}`, {
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
| `dataTypeId` | string | yes | Data type identifier to retrieve, for example TAVG. Example: `TAVG`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datacoverage": 1,
      "id": "string",
      "maxdate": "2026-05-07T12:00:00.000Z",
      "mindate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datacoverage` | number |  |
| `id` | string |  |
| `maxdate` | date |  |
| `mindate` | date |  |
| `name` | string |  |

## Native endpoint

Through the native NCEI Climate Data API, this operation is `GET /datatypes/[:dataTypeId]` (base URL `https://www.ncei.noaa.gov/cdo-web/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-type.md) for the provider-specific parameters and requirements.

