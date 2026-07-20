# ForceManager: Update Activity

Updates an existing activity in ForceManager.

```
PUT https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/update-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ForceManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/update-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/update-activity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Unique identifier for the activity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "activityDateTime": "2026-05-07T12:00:00.000Z",
      "comment": "string",
      "contactId": 1,
      "id": 1,
      "isCheckin": true,
      "salesRepId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number | ID of the account this activity is assigned to. |
| `activityDateTime` | date | Date and time of the activity. |
| `comment` | string | Comments for the activity. |
| `contactId` | number | ID of the contact this activity is assigned to. |
| `id` | number | Unique identifier for the activity. |
| `isCheckin` | boolean | Whether this is a check-in activity. |
| `salesRepId` | number | ID of the sales rep user this activity has been created for. |

## Native endpoint

Through the native ForceManager API, this operation is `PUT /activities`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-activity.md) for the provider-specific parameters and requirements.

