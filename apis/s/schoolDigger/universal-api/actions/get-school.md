# SchoolDigger: Get School

Retrieves a school from SchoolDigger.

```
GET https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/get-school
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SchoolDigger `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/get-school?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/get-school?${params}`, {
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
| `id` | string | yes | Twelve-digit SchoolDigger school ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "chronicAbsenteeismRates": [
        {}
      ],
      "district": {},
      "dropoutRates": [
        {}
      ],
      "finance": [
        {}
      ],
      "graduationRates": [
        {}
      ],
      "locale": "string",
      "phone": "string",
      "rankHistory": [
        {}
      ],
      "reviews": [
        {}
      ],
      "schoolid": "string",
      "schoolLevel": "string",
      "schoolName": "Ava Chen",
      "schoolYearlyDetails": [
        {}
      ],
      "testScores": [
        {}
      ],
      "urlSchoolDigger": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `chronicAbsenteeismRates` | array<object> |  |
| `district` | object |  |
| `dropoutRates` | array<object> |  |
| `finance` | array<object> |  |
| `graduationRates` | array<object> |  |
| `locale` | string |  |
| `phone` | string |  |
| `rankHistory` | array<object> |  |
| `reviews` | array<object> |  |
| `schoolid` | string |  |
| `schoolLevel` | string |  |
| `schoolName` | string |  |
| `schoolYearlyDetails` | array<object> |  |
| `testScores` | array<object> |  |
| `urlSchoolDigger` | string |  |

## Native endpoint

Through the native SchoolDigger API, this operation is `GET /schools/:id` (base URL `https://api.schooldigger.com/v2.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-school.md) for the provider-specific parameters and requirements.

