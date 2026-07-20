# CoachAccountable: Update Engagement

Updates an engagement in CoachAccountable.

```
PUT https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/update-engagement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/update-engagement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "engagementId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/update-engagement', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "engagementId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engagementId` | number | yes |  |
| `name` | string | no |  |
| `startDate` | date | no |  |
| `endDate` | date | no | If provided but set to an empty or otherwise invalid date, the Engagement will be set to continue indefinitely. |
| `allocation` | string | no | The new allocation of the Engagement expressed as a number followed by a space followed by the unit, either "A" for Appointments or "H" for hours (e.g. "12 A" or "6 H"). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CoachAccountable API returns.

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-engagement.md) for the provider-specific parameters and requirements.

