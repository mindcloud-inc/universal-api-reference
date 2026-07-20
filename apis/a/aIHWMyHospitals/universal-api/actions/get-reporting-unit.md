# AIHW MyHospitals: Get Reporting Unit

Retrieves a reporting unit from AIHW MyHospitals.

```
GET https://connect.mindcloud.co/v1/universal/aIHWMyHospitals/latest/actions/get-reporting-unit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AIHW MyHospitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aIHWMyHospitals/latest/actions/get-reporting-unit?connectionId=$CONNECTION_ID&reportingUnitCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reportingUnitCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aIHWMyHospitals/latest/actions/get-reporting-unit?${params}`, {
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
| `reportingUnitCode` | string | yes | The reporting unit code. |

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
| `result` | object | Reporting unit result object returned by the AIHW API. |
| `version_information` | object | AIHW API and data version metadata. |

## Native endpoint

Through the native AIHW MyHospitals API, this operation is `GET /api/v1/reporting-units/{reporting-unit-code}` (base URL `https://myhospitalsapi.aihw.gov.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reporting-unit.md) for the provider-specific parameters and requirements.

