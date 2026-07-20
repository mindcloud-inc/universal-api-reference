# SurveyMethods: Get User Details



```
GET https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/get-user-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveyMethods `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/get-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/get-user-details?${params}`, {
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
      "rowcount": 1,
      "status": "string",
      "user": {
        "account_type": "string",
        "expires_on": "2026-05-07T12:00:00.000Z",
        "license": {
          "license_expires_on": "2026-05-07T12:00:00.000Z",
          "total_licenses": 1,
          "used_licenses": 1
        },
        "member_since": "2026-05-07T12:00:00.000Z",
        "subscription_status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rowcount` | number |  |
| `status` | string |  |
| `user` | object |  |
| `user.account_type` | string |  |
| `user.expires_on` | date |  |
| `user.license` | object |  |
| `user.license.license_expires_on` | date |  |
| `user.license.total_licenses` | number |  |
| `user.license.used_licenses` | number |  |
| `user.member_since` | date |  |
| `user.subscription_status` | string |  |

## Native endpoint

Through the native SurveyMethods API, this operation is `GET /:loginId/:apiKey/users/details/` (base URL `https://api.surveymethods.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-details.md) for the provider-specific parameters and requirements.

