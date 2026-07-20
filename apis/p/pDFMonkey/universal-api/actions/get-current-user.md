# PDFMonkey: Get Current User

Retrieves the current user from PDFMonkey.

```
GET https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDFMonkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/get-current-user?${params}`, {
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
      "currentUser": {
        "availableDocuments": 1,
        "blockResources": true,
        "companyName": "Ava Chen",
        "country": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "currentPlan": "string",
        "currentPlanInterval": "string",
        "desiredName": "Ava Chen",
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "lang": "string",
        "lastName": "Chen",
        "onboardingCompletedAt": "2026-05-07T12:00:00.000Z",
        "payingCustomer": true,
        "phoneNumber": "string",
        "shareLinks": true,
        "trialEndsOn": "2026-05-07T12:00:00.000Z",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "useCase": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentUser.availableDocuments` | number | Remaining or available document quota. |
| `currentUser.blockResources` | boolean | Whether account resources are blocked. |
| `currentUser.companyName` | string | Company name on the account. |
| `currentUser.country` | string | Country code for the account. |
| `currentUser.createdAt` | date | Creation timestamp. |
| `currentUser.currentPlan` | string | Current subscription plan. |
| `currentUser.currentPlanInterval` | string | Billing interval for the current plan. |
| `currentUser.desiredName` | string | Desired account display name. |
| `currentUser.email` | string | Account email address. |
| `currentUser.firstName` | string | First name. |
| `currentUser.id` | string | Current user ID. |
| `currentUser.lang` | string | Preferred language. |
| `currentUser.lastName` | string | Last name. |
| `currentUser.onboardingCompletedAt` | date | Onboarding completion timestamp. |
| `currentUser.payingCustomer` | boolean | Whether the account is a paying customer. |
| `currentUser.phoneNumber` | string | Phone number. |
| `currentUser.shareLinks` | boolean | Whether share links are enabled. |
| `currentUser.trialEndsOn` | date | Trial end date. |
| `currentUser.updatedAt` | date | Last update timestamp. |
| `currentUser.useCase` | string | Declared product use case. |

## Native endpoint

Through the native PDFMonkey API, this operation is `GET /current_user` (base URL `https://api.pdfmonkey.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

