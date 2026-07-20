# SchoolDigger: Get District

Retrieves a district from SchoolDigger.

```
GET https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/get-district
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SchoolDigger `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/get-district?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/get-district?${params}`, {
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
| `id` | string | yes | Seven-digit SchoolDigger district ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "boundary": {},
      "chronicAbsenteeismRates": [
        {}
      ],
      "districtID": "string",
      "districtName": "Ava Chen",
      "districtYearlyDetails": [
        {}
      ],
      "dropoutRates": [
        {}
      ],
      "finance": [
        {}
      ],
      "graduationRates": [
        {}
      ],
      "phone": "string",
      "rankHistory": [
        {}
      ],
      "testScores": [
        {}
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `boundary` | object |  |
| `chronicAbsenteeismRates` | array<object> |  |
| `districtID` | string |  |
| `districtName` | string |  |
| `districtYearlyDetails` | array<object> |  |
| `dropoutRates` | array<object> |  |
| `finance` | array<object> |  |
| `graduationRates` | array<object> |  |
| `phone` | string |  |
| `rankHistory` | array<object> |  |
| `testScores` | array<object> |  |
| `url` | string |  |

## Native endpoint

Through the native SchoolDigger API, this operation is `GET /districts/:id` (base URL `https://api.schooldigger.com/v2.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-district.md) for the provider-specific parameters and requirements.

