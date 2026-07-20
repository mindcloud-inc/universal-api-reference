# HelpDesk: List Subscriptions

Retrieves subscriptions from HelpDesk.

```
GET https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-subscriptions?${params}`, {
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
      "activatedAt": "2026-05-07T12:00:00.000Z",
      "cancelledAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currentPeriodEndsAt": "2026-05-07T12:00:00.000Z",
      "currentPeriodStartedAt": "2026-05-07T12:00:00.000Z",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "planCode": "string",
      "quantity": 1,
      "state": "string",
      "subscriptionID": "string",
      "trialEndsAt": "2026-05-07T12:00:00.000Z",
      "trialStartedAt": "2026-05-07T12:00:00.000Z",
      "unitAmountInCents": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activatedAt` | date |  |
| `cancelledAt` | date |  |
| `createdAt` | date |  |
| `currentPeriodEndsAt` | date |  |
| `currentPeriodStartedAt` | date |  |
| `expiresAt` | date |  |
| `planCode` | string |  |
| `quantity` | number |  |
| `state` | string |  |
| `subscriptionID` | string |  |
| `trialEndsAt` | date |  |
| `trialStartedAt` | date |  |
| `unitAmountInCents` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native HelpDesk API, this operation is `GET /v1/subscriptions` (base URL `https://api.helpdesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

