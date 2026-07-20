# AIHW MyHospitals: List Flat Data Extract

Retrieves flat data for a measure category from AIHW MyHospitals.

```
GET https://connect.mindcloud.co/v1/universal/aIHWMyHospitals/latest/actions/list-flat-data-extract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AIHW MyHospitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aIHWMyHospitals/latest/actions/list-flat-data-extract?connectionId=$CONNECTION_ID&measureCategoryCode=string&skip=0&top=100" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "measureCategoryCode": "string",
  "skip": "0",
  "top": "100"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aIHWMyHospitals/latest/actions/list-flat-data-extract?${params}`, {
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
| `measureCategoryCode` | string | yes | The measure category code. |
| `skip` | number | yes | The number of records to skip. Default: `0`. |
| `top` | number | yes | The number of records to take. Must be between 1 and 1000. Default: `100`. |
| `measureCode` | string | no | Only include data matching the specified measure codes. Accepts multiple values as an array. |
| `reportingUnitCode` | string | no | Only include data for the specified reporting unit codes. Accepts multiple values as an array. |
| `reportingUnitTypeCode` | string | no | Only include data for the specified reporting unit types. Accepts multiple values as an array. |
| `startDate` | string | no | Only include data after this date. Use yyyy, yyyy-MM, or yyyy-MM-dd. |
| `endDate` | string | no | Only include data before this date. Use yyyy, yyyy-MM, or yyyy-MM-dd. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {},
      "version_information": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object | Paginated flat data extract object with data and pagination fields. |
| `version_information` | object | AIHW API and data version metadata. |

## Native endpoint

Through the native AIHW MyHospitals API, this operation is `GET /api/v1/flat-data-extract/{measure-category-code}` (base URL `https://myhospitalsapi.aihw.gov.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-flat-data-extract.md) for the provider-specific parameters and requirements.

