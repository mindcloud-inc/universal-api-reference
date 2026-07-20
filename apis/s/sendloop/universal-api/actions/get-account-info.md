# Sendloop: Get Account Info



```
GET https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendloop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/get-account-info?${params}`, {
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
      "city": "string",
      "companyName": "Ava Chen",
      "country": "string",
      "email": "ava@example.com",
      "emailVerificationStatus": "ava@example.com",
      "fax": "string",
      "firstName": "Ava",
      "language": "string",
      "lastAccountUpdateDate": "2026-05-07T12:00:00.000Z",
      "lastActivityDateTime": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "memberSince": "2026-05-07T12:00:00.000Z",
      "phone": "string",
      "signUpIP": "string",
      "state": "string",
      "street": "string",
      "subdomain": "string",
      "timeZone": "string",
      "username": "Ava Chen",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `companyName` | string |  |
| `country` | string |  |
| `email` | string |  |
| `emailVerificationStatus` | string |  |
| `fax` | string |  |
| `firstName` | string |  |
| `language` | string |  |
| `lastAccountUpdateDate` | date |  |
| `lastActivityDateTime` | date |  |
| `lastName` | string |  |
| `memberSince` | date |  |
| `phone` | string |  |
| `signUpIP` | string |  |
| `state` | string |  |
| `street` | string |  |
| `subdomain` | string |  |
| `timeZone` | string |  |
| `username` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Sendloop API, this operation is `POST /account.info.get/json` (base URL `https://{{credentials.subdomain}}.sendloop.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.

