# ClassMarker: List Recent Results for All Groups



```
GET https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/list-recent-results-for-all-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClassMarker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/list-recent-results-for-all-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/list-recent-results-for-all-groups?${params}`, {
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
| `finishedAfterTimestamp` | date | no | Only include results finished after this time. The wrapper converts the selected date to the UNIX timestamp format required by ClassMarker. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "finishedAfterTimestampUsed": 1,
      "groups": [
        {
          "group": {
            "groupId": 1,
            "groupName": "Ava Chen"
          }
        }
      ],
      "nextFinishedAfterTimestamp": 1,
      "results": [
        {
          "result": {
            "email": "ava@example.com",
            "first": "string",
            "groupId": 1,
            "last": "string",
            "percentage": 1,
            "pointsAvailable": 1,
            "pointsScored": 1,
            "status": "string",
            "testId": 1,
            "timeFinished": 1,
            "timeStarted": 1,
            "userId": 1
          }
        }
      ],
      "tests": [
        {
          "test": {
            "testId": 1,
            "testName": "Ava Chen"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `finishedAfterTimestampUsed` | number |  |
| `groups[].group.groupId` | number |  |
| `groups[].group.groupName` | string |  |
| `nextFinishedAfterTimestamp` | number |  |
| `results[].result.email` | string |  |
| `results[].result.first` | string |  |
| `results[].result.groupId` | number |  |
| `results[].result.last` | string |  |
| `results[].result.percentage` | number |  |
| `results[].result.pointsAvailable` | number |  |
| `results[].result.pointsScored` | number |  |
| `results[].result.status` | string |  |
| `results[].result.testId` | number |  |
| `results[].result.timeFinished` | number |  |
| `results[].result.timeStarted` | number |  |
| `results[].result.userId` | number |  |
| `tests[].test.testId` | number |  |
| `tests[].test.testName` | string |  |

## Native endpoint

Through the native ClassMarker API, this operation is `GET /v1/groups/recent_results.json` (base URL `https://api.classmarker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recent-results-for-all-groups.md) for the provider-specific parameters and requirements.

