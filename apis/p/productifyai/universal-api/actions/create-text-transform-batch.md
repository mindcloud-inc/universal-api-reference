# Productify.ai: Create Text Transform Batch



```
POST https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/create-text-transform-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productify.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/create-text-transform-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transformInputs[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/create-text-transform-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transformInputs[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transformInputs[]` | array<object> | yes | Text inputs to transform in the batch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchId": 1,
      "batchSizeLimitExceeded": true,
      "creditCost": 1,
      "creditLimitReached": true,
      "creditsRemaining": 1,
      "currentBalance": 1,
      "responseMessage": "string",
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
| `batchId` | number |  |
| `batchSizeLimitExceeded` | boolean |  |
| `creditCost` | number |  |
| `creditLimitReached` | boolean |  |
| `creditsRemaining` | number |  |
| `currentBalance` | number |  |
| `responseMessage` | string |  |
| `validationResults` | array<object> |  |
| `validations` | array<object> |  |
| `wasSuccessful` | boolean |  |

## Native endpoint

Through the native Productify.ai API, this operation is `POST /Batch/Transform` (base URL `https://api.productify.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-text-transform-batch.md) for the provider-specific parameters and requirements.

