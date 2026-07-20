# DocuWriter.ai: Get User Info



```
GET https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/get-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuWriter.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/get-user-info?${params}`, {
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
      "email": "ava@example.com",
      "id": 1,
      "isOnTrial": true,
      "name": "Ava Chen",
      "remainingCredits": 1,
      "subscriptionStatus": "string",
      "teamRole": "string",
      "trialEndsAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | User email address. |
| `id` | number | User ID. |
| `isOnTrial` | boolean | Whether the account is currently on trial. |
| `name` | string | User display name. |
| `remainingCredits` | number | Remaining DocuWriter credits on the account. |
| `subscriptionStatus` | string | Current subscription status when available. |
| `teamRole` | string | Role of the current user within the team when available. |
| `trialEndsAt` | date | Trial end timestamp when the account is on trial. |

## Native endpoint

Through the native DocuWriter.ai API, this operation is `GET /api/user-info` (base URL `https://app.docuwriter.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-info.md) for the provider-specific parameters and requirements.

