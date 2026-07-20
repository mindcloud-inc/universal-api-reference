# Kite Suite: Get all automation histories



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-all-automation-histories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-all-automation-histories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-all-automation-histories?${params}`, {
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
      "actionData": {},
      "automationID": "string",
      "errorLog": "string",
      "status": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionData` | object |  |
| `automationID` | string |  |
| `errorLog` | string |  |
| `status` | string |  |
| `workspace` | string |  |

## Native endpoint

Through the native Kite Suite API, this operation is `GET /api/v1/automation/history` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-automation-histories.md) for the provider-specific parameters and requirements.

