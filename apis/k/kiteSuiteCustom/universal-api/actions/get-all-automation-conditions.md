# Kite Suite: Get all automation conditions



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-all-automation-conditions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-all-automation-conditions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-all-automation-conditions?${params}`, {
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
      "actions": [
        "string"
      ],
      "createdBy": "string",
      "description": "string",
      "events": [
        "string"
      ],
      "eventType": "string",
      "isActive": true,
      "isTrashed": true,
      "trigger": {},
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions` | array |  |
| `createdBy` | string | The ID of the user who created the automation |
| `description` | string |  |
| `events` | array |  |
| `eventType` | string | The type of event |
| `isActive` | boolean |  |
| `isTrashed` | boolean |  |
| `trigger` | object |  |
| `workspace` | string | The ID of the workspace |

## Native endpoint

Through the native Kite Suite API, this operation is `GET /api/v1/automation` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-automation-conditions.md) for the provider-specific parameters and requirements.

