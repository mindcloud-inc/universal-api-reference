# Zoho PageSense: Create Goal for Experiment

Creates an experiment goal in Zoho PageSense.

```
POST https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/create-goal-for-experiment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho PageSense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/create-goal-for-experiment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "portalName": "Ava Chen",
  "goal.displayName": "Ava Chen",
  "goal.goalType": 1,
  "goal.projectLinkname": "https://example.com",
  "goal.experimentLinkname": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/create-goal-for-experiment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "portalName": "Ava Chen",
    "goal.displayName": "Ava Chen",
    "goal.goalType": 1,
    "goal.projectLinkname": "https://example.com",
    "goal.experimentLinkname": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `portalName` | string | yes | Portal identifier in the path. |
| `goal.displayName` | string | yes | Human-readable goal name. |
| `goal.goalType` | number | yes | Goal type code from Zoho PageSense. |
| `goal.projectLinkname` | string | yes | Project linkname for the goal. |
| `goal.experimentLinkname` | string | yes | Experiment linkname for the goal. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "goals": [
        {
          "displayName": "Ava Chen",
          "goalId": 1,
          "linkname": "https://example.com",
          "success": true
        }
      ],
      "statusCode": "string",
      "statusString": "string",
      "timeTakenToProcessTheRequest": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `goals[].displayName` | string |  |
| `goals[].goalId` | number |  |
| `goals[].linkname` | string |  |
| `goals[].success` | boolean |  |
| `statusCode` | string |  |
| `statusString` | string |  |
| `timeTakenToProcessTheRequest` | string |  |

## Native endpoint

Through the native Zoho PageSense API, this operation is `POST /portal/:portalName/goals` (base URL `https://pagesense.zoho.com/pagesense/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-goal-for-experiment.md) for the provider-specific parameters and requirements.

