# Optimizely: Get Plan

Retrieves plan and usage information from Optimizely.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-plan?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-plan?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "planName": "Ava Chen",
      "productUsages": [
        {}
      ],
      "status": "string",
      "unitOfMeasurement": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `planName` | string |  |
| `productUsages` | array<object> |  |
| `status` | string |  |
| `unitOfMeasurement` | string |  |

## Native endpoint

Through the native Optimizely API, this operation is `GET /plan` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-plan.md) for the provider-specific parameters and requirements.

