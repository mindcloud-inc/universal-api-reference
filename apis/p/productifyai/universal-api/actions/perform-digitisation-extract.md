# Productify.ai: Perform Digitisation Extract



```
POST https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/perform-digitisation-extract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productify.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/perform-digitisation-extract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/perform-digitisation-extract', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input` | object | yes | Image input to extract data from. |

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

Through the native Productify.ai API, this operation is `POST /Single/Extract` (base URL `https://api.productify.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/perform-digitisation-extract.md) for the provider-specific parameters and requirements.

