# GetTranscribe: Get User Info

Retrieves user account details from GetTranscribe.

```
GET https://connect.mindcloud.co/v1/universal/getTranscribe/latest/actions/get-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetTranscribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getTranscribe/latest/actions/get-user-info?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getTranscribe/latest/actions/get-user-info?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The ID of the user to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiMinutesLimit": 1,
      "autoRechargeAmount": 1,
      "autoRechargeThreshold": 1,
      "balance": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currentUsageMessages": 1,
      "currentUsageMinutes": 1,
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "demoTranscriptionSessionId": "string",
      "email": "ava@example.com",
      "enableAutoRecharge": true,
      "firstName": "Ava",
      "googleId": "string",
      "id": 1,
      "lastName": "Chen",
      "messagesLimit": 1,
      "minutesLimit": 1,
      "onboardingCompleted": true,
      "profilePicture": "string",
      "purchasedMessagesBalance": 1,
      "purchasedMinutesBalance": 1,
      "subscriptionAmount": "string",
      "subscriptionCurrentPeriodEnd": "2026-05-07T12:00:00.000Z",
      "subscriptionCurrentPeriodStart": "2026-05-07T12:00:00.000Z",
      "subscriptionPlanName": "Ava Chen",
      "subscriptionStatus": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiMinutesLimit` | number |  |
| `autoRechargeAmount` | number |  |
| `autoRechargeThreshold` | number |  |
| `balance` | string |  |
| `createdAt` | date |  |
| `currentUsageMessages` | number |  |
| `currentUsageMinutes` | number |  |
| `deletedAt` | date |  |
| `demoTranscriptionSessionId` | string |  |
| `email` | string |  |
| `enableAutoRecharge` | boolean |  |
| `firstName` | string |  |
| `googleId` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `messagesLimit` | number |  |
| `minutesLimit` | number |  |
| `onboardingCompleted` | boolean |  |
| `profilePicture` | string |  |
| `purchasedMessagesBalance` | number |  |
| `purchasedMinutesBalance` | number |  |
| `subscriptionAmount` | string |  |
| `subscriptionCurrentPeriodEnd` | date |  |
| `subscriptionCurrentPeriodStart` | date |  |
| `subscriptionPlanName` | string |  |
| `subscriptionStatus` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native GetTranscribe API, this operation is `GET /users/:id` (base URL `https://api.gettranscribe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-info.md) for the provider-specific parameters and requirements.

