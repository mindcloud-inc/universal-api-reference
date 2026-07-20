# Zillow Public Records: List assessments

Retrieves public property assessments from Zillow Public Records.

```
GET https://connect.mindcloud.co/v1/universal/zillowPublicRecords/latest/actions/list-assessments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zillow Public Records `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowPublicRecords/latest/actions/list-assessments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zillowPublicRecords/latest/actions/list-assessments?${params}`, {
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
| `zpid` | string | no | Zillow property ID to narrow the public records assessment search. |
| `addressFull` | string | no | Full property address to narrow the public records assessment search. Default: `123 Main Street`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sortBy` | string | no | Assessment field to sort the returned records by, such as year. Default: `year`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "apn": "string",
      "areas": [
        {}
      ],
      "BridgeModificationTimestamp": "2026-05-07T12:00:00.000Z",
      "building": [
        {}
      ],
      "coordinates": [
        1
      ],
      "county": "string",
      "fips": "string",
      "id": "string",
      "improvementValue": 1,
      "landUseCode": "string",
      "landUseDescription": "string",
      "landValue": 1,
      "taxYear": 1,
      "totalValue": 1,
      "zoning": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object | Structured address object. |
| `apn` | string | Assessor Parcel Number. |
| `areas` | array<object> | Area detail records. |
| `BridgeModificationTimestamp` | date | Timestamp for the latest Bridge-side modification. |
| `building` | array<object> | Building detail records. |
| `coordinates` | array<number> | Longitude and latitude coordinates. |
| `county` | string | County name. |
| `fips` | string | Five-digit county FIPS code. |
| `id` | string | Unique assessment identifier. |
| `improvementValue` | number | Assessed improvement value. |
| `landUseCode` | string | Land use code. |
| `landUseDescription` | string | Land use description. |
| `landValue` | number | Assessed land value. |
| `taxYear` | number | Tax year. |
| `totalValue` | number | Total assessed value. |
| `zoning` | string | Zoning designation. |

## Native endpoint

Through the native Zillow Public Records API, this operation is `GET /pub/assessments` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assessments.md) for the provider-specific parameters and requirements.

