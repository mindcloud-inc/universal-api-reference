# Dashcam: Get Parallel Slots

Retrieves parallel slot details from Dashcam.

```
GET https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/get-parallel-slots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dashcam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/get-parallel-slots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/get-parallel-slots?${params}`, {
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
      "activeSandboxes": 1,
      "includedMinutes": 1,
      "includedSeconds": 1,
      "maxConcurrentSandboxes": 1,
      "plan": "string",
      "remainingMinutes": 1,
      "remainingSeconds": 1,
      "totalUsedMinutes": 1,
      "totalUsedSeconds": 1,
      "unlimited": true,
      "usagePercentage": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeSandboxes` | number |  |
| `includedMinutes` | number |  |
| `includedSeconds` | number |  |
| `maxConcurrentSandboxes` | number |  |
| `plan` | string |  |
| `remainingMinutes` | number |  |
| `remainingSeconds` | number |  |
| `totalUsedMinutes` | number |  |
| `totalUsedSeconds` | number |  |
| `unlimited` | boolean |  |
| `usagePercentage` | number |  |

## Native endpoint

Through the native Dashcam API, this operation is `GET /api/billing/parallel-slots` (base URL `https://api.testdriver.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-parallel-slots.md) for the provider-specific parameters and requirements.

