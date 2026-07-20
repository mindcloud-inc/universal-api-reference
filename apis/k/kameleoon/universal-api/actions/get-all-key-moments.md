# Kameleoon: Get all key moments



```
GET https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-key-moments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kameleoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-key-moments?connectionId=$CONNECTION_ID&paramsIo=page%3D1%2C%20perPage%3D20" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paramsIo": "page=1, perPage=20"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-key-moments?${params}`, {
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
| `paramsIo` | string | yes | Required query object documented by Kameleoon for list endpoints. Example: `page=1, perPage=20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audienceTracking": true,
      "conditionDataList": [
        {}
      ],
      "htmlDescription": "string",
      "id": 1,
      "isConditionBlock": true,
      "logicalOperator": "string",
      "name": "Ava Chen",
      "parentId": 1,
      "targetingCondition": {},
      "targetingType": "string",
      "weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audienceTracking` | boolean |  |
| `conditionDataList` | array<object> |  |
| `htmlDescription` | string |  |
| `id` | number |  |
| `isConditionBlock` | boolean |  |
| `logicalOperator` | string |  |
| `name` | string |  |
| `parentId` | number |  |
| `targetingCondition` | object |  |
| `targetingType` | string |  |
| `weight` | number |  |

## Native endpoint

Through the native Kameleoon API, this operation is `GET key-moments` (base URL `https://api.kameleoon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-key-moments.md) for the provider-specific parameters and requirements.

