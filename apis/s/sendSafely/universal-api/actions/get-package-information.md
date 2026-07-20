# SendSafely: Get Package Information



```
GET https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/get-package-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendSafely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/get-package-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/get-package-information?${params}`, {
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
      "approverList": [
        {}
      ],
      "contactGroups": [
        {}
      ],
      "directories": [
        {}
      ],
      "files": [
        {}
      ],
      "isArchived": true,
      "isVDR": true,
      "life": 1,
      "needsApproval": true,
      "packageCode": "string",
      "packageId": "string",
      "packageSender": "string",
      "packageTimestamp": "string",
      "passwordRequired": true,
      "recipients": [
        {}
      ],
      "response": "string",
      "rootDirectoryId": "string",
      "serverSecret": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approverList` | array<object> |  |
| `contactGroups` | array<object> |  |
| `directories` | array<object> |  |
| `files` | array<object> |  |
| `isArchived` | boolean |  |
| `isVDR` | boolean |  |
| `life` | number |  |
| `needsApproval` | boolean |  |
| `packageCode` | string |  |
| `packageId` | string |  |
| `packageSender` | string |  |
| `packageTimestamp` | string |  |
| `passwordRequired` | boolean |  |
| `recipients` | array<object> |  |
| `response` | string |  |
| `rootDirectoryId` | string |  |
| `serverSecret` | string |  |
| `state` | string |  |

## Native endpoint

Through the native SendSafely API, this operation is `GET /package/:packageId/` (base URL `https://app.sendsafely.com/api/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-package-information.md) for the provider-specific parameters and requirements.

