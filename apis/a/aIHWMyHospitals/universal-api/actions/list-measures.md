# AIHW MyHospitals: List Measures

Retrieves all measures from AIHW MyHospitals.

```
GET https://connect.mindcloud.co/v1/universal/aIHWMyHospitals/latest/actions/list-measures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AIHW MyHospitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aIHWMyHospitals/latest/actions/list-measures?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aIHWMyHospitals/latest/actions/list-measures?${params}`, {
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
| `measureCategoryCode` | string | no | Only include measures matching the specified measure category codes. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": [
        {}
      ],
      "version_information": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | array<object> | Measure objects returned by the AIHW API. |
| `version_information` | object | AIHW API and data version metadata. |

## Native endpoint

Through the native AIHW MyHospitals API, this operation is `GET /api/v1/measures` (base URL `https://myhospitalsapi.aihw.gov.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-measures.md) for the provider-specific parameters and requirements.

