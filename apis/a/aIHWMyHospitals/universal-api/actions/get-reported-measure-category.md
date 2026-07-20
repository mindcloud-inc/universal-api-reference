# AIHW MyHospitals: Get Reported Measure Category

Retrieves a reported measure category from AIHW MyHospitals.

```
GET https://connect.mindcloud.co/v1/universal/aIHWMyHospitals/latest/actions/get-reported-measure-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AIHW MyHospitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aIHWMyHospitals/latest/actions/get-reported-measure-category?connectionId=$CONNECTION_ID&reportedMeasureCategoryCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reportedMeasureCategoryCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aIHWMyHospitals/latest/actions/get-reported-measure-category?${params}`, {
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
| `reportedMeasureCategoryCode` | string | yes | The reported measure category code. |

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
| `result` | object | Reported measure category result object returned by the AIHW API. |
| `version_information` | object | AIHW API and data version metadata. |

## Native endpoint

Through the native AIHW MyHospitals API, this operation is `GET /api/v1/reported-measure-categories/{reported-measure-category-code}` (base URL `https://myhospitalsapi.aihw.gov.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reported-measure-category.md) for the provider-specific parameters and requirements.

