# Zoho PageSense: Delete Goal for Experiment

Deletes an experiment goal from Zoho PageSense.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/delete-goal-for-experiment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho PageSense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/delete-goal-for-experiment?connectionId=$CONNECTION_ID&portalName=Ava%20Chen&goalLinkname=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalName": "Ava Chen",
  "goalLinkname": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/delete-goal-for-experiment?${params}`, {
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
| `portalName` | string | yes | Portal identifier in the path. |
| `goalLinkname` | string | yes | Goal linkname in the path. |

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

Through the native Zoho PageSense API, this operation is `DELETE /portal/:portalName/goals/:goalLinkname` (base URL `https://pagesense.zoho.com/pagesense/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-goal-for-experiment.md) for the provider-specific parameters and requirements.

