# Intruder: List Issue Occurrences



```
GET https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-issue-occurrences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intruder `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-issue-occurrences?connectionId=$CONNECTION_ID&limit=25&offset=0&issueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "issueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-issue-occurrences?${params}`, {
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
| `issueId` | string | yes | The Intruder issue identifier. |
| `since` | string | no | Filter occurrences first detected on or after this timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "age": "string",
      "cves": [
        "string"
      ],
      "cvssScore": 1,
      "displayAddress": "string",
      "exploitLikelihood": "string",
      "extraInfo": {},
      "firstSeenAt": "string",
      "id": 1,
      "occurrenceId": 1,
      "port": "string",
      "protocol": "string",
      "snoozed": true,
      "snoozeReason": "string",
      "snoozeUntil": "string",
      "target": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age` | string |  |
| `cves` | array<string> |  |
| `cvssScore` | number |  |
| `displayAddress` | string |  |
| `exploitLikelihood` | string |  |
| `extraInfo` | object |  |
| `firstSeenAt` | string |  |
| `id` | number |  |
| `occurrenceId` | number |  |
| `port` | string |  |
| `protocol` | string |  |
| `snoozed` | boolean |  |
| `snoozeReason` | string |  |
| `snoozeUntil` | string |  |
| `target` | string |  |

## Native endpoint

Through the native Intruder API, this operation is `GET /issues/:issueId/occurrences/` (base URL `https://api.intruder.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-issue-occurrences.md) for the provider-specific parameters and requirements.

