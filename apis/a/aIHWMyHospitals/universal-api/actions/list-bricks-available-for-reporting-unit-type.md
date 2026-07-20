# AIHW MyHospitals: List Bricks Available For Reporting Unit Type

Retrieves available bricks by reporting unit for a type in AIHW MyHospitals.

```
GET https://connect.mindcloud.co/v1/universal/aIHWMyHospitals/latest/actions/list-bricks-available-for-reporting-unit-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AIHW MyHospitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aIHWMyHospitals/latest/actions/list-bricks-available-for-reporting-unit-type?connectionId=$CONNECTION_ID&reportingUnitTypeCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reportingUnitTypeCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aIHWMyHospitals/latest/actions/list-bricks-available-for-reporting-unit-type?${params}`, {
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
| `reportingUnitTypeCode` | string | yes | The reporting unit type code. |

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
| `result` | object | Dictionary of reporting unit codes to available brick-code arrays. |
| `version_information` | object | AIHW API and data version metadata. |

## Native endpoint

Through the native AIHW MyHospitals API, this operation is `GET /api/v1/reporting-unit-types/{reporting-unit-type-code}/bricks-available` (base URL `https://myhospitalsapi.aihw.gov.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bricks-available-for-reporting-unit-type.md) for the provider-specific parameters and requirements.

