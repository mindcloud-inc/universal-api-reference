# Intruder: List Issues



```
GET https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intruder `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-issues?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-issues?${params}`, {
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
| `since` | string | no | Filter issues first detected on or after this timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cvssScore": 1,
      "description": "string",
      "exploitLikelihood": "string",
      "id": 1,
      "occurrences": "string",
      "remediation": "string",
      "severity": "string",
      "snoozed": true,
      "snoozeReason": "string",
      "snoozeUntil": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cvssScore` | number |  |
| `description` | string |  |
| `exploitLikelihood` | string |  |
| `id` | number |  |
| `occurrences` | string |  |
| `remediation` | string |  |
| `severity` | string |  |
| `snoozed` | boolean |  |
| `snoozeReason` | string |  |
| `snoozeUntil` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Intruder API, this operation is `GET /issues/` (base URL `https://api.intruder.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-issues.md) for the provider-specific parameters and requirements.

