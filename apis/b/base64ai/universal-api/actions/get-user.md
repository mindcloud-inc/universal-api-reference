# Base64.ai: Get User

Retrieves user account details from Base64.ai.

```
GET https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Base64.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/get-user?${params}`, {
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
      "ccEmails": [
        "ava@example.com"
      ],
      "companyName": "Ava Chen",
      "defaultFlowID": "string",
      "email": "ava@example.com",
      "familyName": "Ava Chen",
      "givenName": "Ava Chen",
      "hasActiveAwsContract": true,
      "hasSponsor": true,
      "isDomainAdmin": true,
      "isWorkEmailVerified": true,
      "numberOfCredits": 1,
      "numberOfCreditsSpentOnDocuments": 1,
      "numberOfPages": 1,
      "numberOfUploads": 1,
      "passkeys": [
        {}
      ],
      "phoneNumber": "string",
      "starred": {},
      "status": "string",
      "subscriptionPeriod": "string",
      "subscriptionType": "string",
      "tags": [
        "string"
      ],
      "tour": {
        "isDisabled": true,
        "welcomeCompleted": 1
      },
      "workEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ccEmails[]` | string |  |
| `companyName` | string |  |
| `defaultFlowID` | string |  |
| `email` | string |  |
| `familyName` | string |  |
| `givenName` | string |  |
| `hasActiveAwsContract` | boolean |  |
| `hasSponsor` | boolean |  |
| `isDomainAdmin` | boolean |  |
| `isWorkEmailVerified` | boolean |  |
| `numberOfCredits` | number |  |
| `numberOfCreditsSpentOnDocuments` | number |  |
| `numberOfPages` | number |  |
| `numberOfUploads` | number |  |
| `passkeys[]` | object |  |
| `phoneNumber` | string |  |
| `starred` | object |  |
| `status` | string |  |
| `subscriptionPeriod` | string |  |
| `subscriptionType` | string |  |
| `tags[]` | string |  |
| `tour.isDisabled` | boolean |  |
| `tour.welcomeCompleted` | number |  |
| `workEmail` | string |  |

## Native endpoint

Through the native Base64.ai API, this operation is `GET /api/auth/user` (base URL `https://base64.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

