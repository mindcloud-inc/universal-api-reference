# Pitchbox: List Opportunity Milestone History



```
GET https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-opportunity-milestone-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-opportunity-milestone-history?connectionId=$CONNECTION_ID&opportunityId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "opportunityId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-opportunity-milestone-history?${params}`, {
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
| `opportunityId` | number | yes | The opportunity id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "milestoneChangeAt": "2026-05-07T12:00:00.000Z",
      "milestoneNew": "string",
      "milestonePrevious": "string",
      "user": {
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": 1,
        "lastName": "Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `milestoneChangeAt` | date |  |
| `milestoneNew` | string |  |
| `milestonePrevious` | string |  |
| `user.displayName` | string |  |
| `user.email` | string |  |
| `user.firstName` | string |  |
| `user.id` | number |  |
| `user.lastName` | string |  |

## Native endpoint

Through the native Pitchbox API, this operation is `GET /api/opportunities/:opportunityId/milestone_history` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-opportunity-milestone-history.md) for the provider-specific parameters and requirements.

