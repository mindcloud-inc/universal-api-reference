# LaunchDarkly: List Flag Statuses

Retrieves feature flag statuses from LaunchDarkly.

```
GET https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/list-flag-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchDarkly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/list-flag-statuses?connectionId=$CONNECTION_ID&environmentKey=string&projectKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "environmentKey": "string",
  "projectKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/list-flag-statuses?${params}`, {
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
| `environmentKey` | string | yes | The LaunchDarkly environment key. |
| `projectKey` | string | yes | The LaunchDarkly project key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lastRequested": "2026-05-07T12:00:00.000Z",
      "links": {},
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lastRequested` | date |  |
| `links` | object |  |
| `name` | string |  |

## Native endpoint

Through the native LaunchDarkly API, this operation is `GET /flag-statuses/:projectKey/:environmentKey` (base URL `https://app.launchdarkly.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-flag-statuses.md) for the provider-specific parameters and requirements.

