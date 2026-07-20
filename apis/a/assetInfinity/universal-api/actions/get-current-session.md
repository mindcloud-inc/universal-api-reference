# Asset Infinity: Get Current Session

Retrieves current session details from Asset Infinity.

```
GET https://connect.mindcloud.co/v1/universal/assetInfinity/latest/actions/get-current-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asset Infinity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assetInfinity/latest/actions/get-current-session?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assetInfinity/latest/actions/get-current-session?${params}`, {
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
      "data": {
        "azureReferenceId": "string",
        "company": "string",
        "createdDate": "2026-05-07T12:00:00.000Z",
        "currency": "string",
        "currencySymbol": "string",
        "customerId": "string",
        "dateFormat": "string",
        "defaultScreen": "string",
        "department": {},
        "deviceId": "string",
        "email": "ava@example.com",
        "expiryDate": "2026-05-07T12:00:00.000Z",
        "isActive": true,
        "isLangReqOnLogin": true,
        "isLangUpdateOnLogin": true,
        "isLocationAccessOnScan": true,
        "isPasswordChangeNeed": true,
        "isScanLogDisable": true,
        "isSingleSession": true,
        "languageCode": "string",
        "mobileNo": {},
        "organisationType": "string",
        "partnerId": 1,
        "paymentReminder": 1,
        "paymentTerm": "string",
        "referenceId": "string",
        "refreshToken": "string",
        "roleId": "string",
        "themeColor": {},
        "timeZone": "string",
        "title": {},
        "token": "string",
        "tokenExpiryMinutes": 1,
        "uid": "string",
        "userMetadata": {},
        "userName": "Ava Chen",
        "userTypeId": "string"
      },
      "isSuccess": true,
      "message": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.azureReferenceId` | string |  |
| `data.company` | string |  |
| `data.createdDate` | date |  |
| `data.currency` | string |  |
| `data.currencySymbol` | string |  |
| `data.customerId` | string |  |
| `data.dateFormat` | string |  |
| `data.defaultScreen` | string |  |
| `data.department` | object |  |
| `data.deviceId` | string |  |
| `data.email` | string |  |
| `data.expiryDate` | date |  |
| `data.isActive` | boolean |  |
| `data.isLangReqOnLogin` | boolean |  |
| `data.isLangUpdateOnLogin` | boolean |  |
| `data.isLocationAccessOnScan` | boolean |  |
| `data.isPasswordChangeNeed` | boolean |  |
| `data.isScanLogDisable` | boolean |  |
| `data.isSingleSession` | boolean |  |
| `data.languageCode` | string |  |
| `data.mobileNo` | object |  |
| `data.organisationType` | string |  |
| `data.partnerId` | number |  |
| `data.paymentReminder` | number |  |
| `data.paymentTerm` | string |  |
| `data.referenceId` | string |  |
| `data.refreshToken` | string |  |
| `data.roleId` | string |  |
| `data.themeColor` | object |  |
| `data.timeZone` | string |  |
| `data.title` | object |  |
| `data.token` | string |  |
| `data.tokenExpiryMinutes` | number |  |
| `data.uid` | string |  |
| `data.userMetadata` | object |  |
| `data.userName` | string |  |
| `data.userTypeId` | string |  |
| `isSuccess` | boolean |  |
| `message` | string |  |
| `statusCode` | number |  |

## Native endpoint

Through the native Asset Infinity API, this operation is `GET auth` (base URL `https://api.assetinfinity.io/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-session.md) for the provider-specific parameters and requirements.

