# Productify.ai: Get Text Transform Batch Results



```
GET https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/get-text-transform-batch-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productify.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/get-text-transform-batch-results?connectionId=$CONNECTION_ID&batchId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "batchId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/get-text-transform-batch-results?${params}`, {
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
| `batchId` | number | yes | Batch identifier to retrieve results for. |
| `pageNumber` | number | no |  |
| `pageSize` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchSizeLimitExceeded": true,
      "creditCost": 1,
      "creditLimitReached": true,
      "creditsRemaining": 1,
      "currentBalance": 1,
      "responseMessage": "string",
      "results": [
        {}
      ],
      "validationResults": [
        {}
      ],
      "validations": [
        {}
      ],
      "wasSuccessful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchSizeLimitExceeded` | boolean |  |
| `creditCost` | number |  |
| `creditLimitReached` | boolean |  |
| `creditsRemaining` | number |  |
| `currentBalance` | number |  |
| `responseMessage` | string |  |
| `results` | array<object> |  |
| `validationResults` | array<object> |  |
| `validations` | array<object> |  |
| `wasSuccessful` | boolean |  |

## Native endpoint

Through the native Productify.ai API, this operation is `POST /Result/Transform` (base URL `https://api.productify.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-text-transform-batch-results.md) for the provider-specific parameters and requirements.

