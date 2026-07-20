# Zoho Survey: Get OAuth User Info

Retrieves connected Zoho account user info for Zoho Survey.

```
GET https://connect.mindcloud.co/v1/universal/zohoSurvey/latest/actions/get-oauth-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Survey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSurvey/latest/actions/get-oauth-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSurvey/latest/actions/get-oauth-user-info?${params}`, {
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
      "Display_Name": "Ava Chen",
      "Email": "ava@example.com",
      "First_Name": "Ava",
      "Last_Name": "Chen",
      "ZUID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Display_Name` | string | Zoho display name from the OAuth user info response. |
| `Email` | string | Zoho email address from the OAuth user info response. |
| `First_Name` | string | Zoho first name from the OAuth user info response. |
| `Last_Name` | string | Zoho last name from the OAuth user info response. |
| `ZUID` | number | Zoho user identifier from the OAuth user info response. |

## Native endpoint

Through the native Zoho Survey API, this operation is `GET {{credentials.authorizeRequest.["accounts-server"]}}/oauth/user/info` (base URL `https://survey.zoho.com/api/v1/external-private`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-oauth-user-info.md) for the provider-specific parameters and requirements.

