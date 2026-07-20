# GoTeamup: Create Offering Type Helper

Creates a new offering type in GoTeamup.

```
POST https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/create-offering-type-helper
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/create-offering-type-helper" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "description": "string",
  "scheduleType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/create-offering-type-helper', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "description": "string",
    "scheduleType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `description` | string | yes |  |
| `scheduleType` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowsDropins": true,
      "backgroundColor": "string",
      "cancellationNoticeInterval": 1,
      "category": {},
      "color": "string",
      "customerVisibility": "string",
      "description": "string",
      "dropinPrice": {},
      "hasActiveSchedules": true,
      "hasPricing": true,
      "id": 1,
      "image": {},
      "instructors": "string",
      "isDraft": true,
      "maxAllowedAge": {},
      "membershipsCount": 1,
      "membershipsSummaryDescription": "string",
      "minAllowedAge": {},
      "name": "Ava Chen",
      "object": "string",
      "order": 1,
      "registrationsCloseInterval": 1,
      "registrationsOpenInterval": 1,
      "scheduleType": "string",
      "status": "string",
      "waitlistMax": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowsDropins` | boolean |  |
| `backgroundColor` | string |  |
| `cancellationNoticeInterval` | number |  |
| `category` | object |  |
| `color` | string |  |
| `customerVisibility` | string |  |
| `description` | string |  |
| `dropinPrice` | object |  |
| `hasActiveSchedules` | boolean |  |
| `hasPricing` | boolean |  |
| `id` | number |  |
| `image` | object |  |
| `instructors` | string |  |
| `isDraft` | boolean |  |
| `maxAllowedAge` | object |  |
| `membershipsCount` | number |  |
| `membershipsSummaryDescription` | string |  |
| `minAllowedAge` | object |  |
| `name` | string |  |
| `object` | string |  |
| `order` | number |  |
| `registrationsCloseInterval` | number |  |
| `registrationsOpenInterval` | number |  |
| `scheduleType` | string |  |
| `status` | string |  |
| `waitlistMax` | object |  |

## Native endpoint

Through the native GoTeamup API, this operation is `POST /offering_types` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-offering-type-helper.md) for the provider-specific parameters and requirements.

