# Asset Infinity Universal API Examples

These examples use the MindCloud API key and Asset Infinity connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Session

Retrieves current session details from Asset Infinity.

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

Example response:

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

See the full [Get Current Session action reference](actions/get-current-session.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/assetInfinity/latest/actions/get-current-session).
