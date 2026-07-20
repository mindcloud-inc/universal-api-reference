# LaunchDarkly: Update Environment

Updates an existing environment in LaunchDarkly.

```
PUT https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/update-environment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchDarkly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/update-environment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "environmentKey": "string",
  "projectKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/update-environment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "environmentKey": "string",
    "projectKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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
      "apiKey": "string",
      "approvalSettings": {},
      "color": "string",
      "confirmChanges": true,
      "critical": true,
      "defaultTrackEvents": true,
      "defaultTtl": 1,
      "id": "string",
      "key": "string",
      "links": {},
      "mobileKey": "string",
      "name": "Ava Chen",
      "requireComments": true,
      "resourceApprovalSettings": {},
      "secureMode": true,
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKey` | string |  |
| `approvalSettings` | object |  |
| `color` | string |  |
| `confirmChanges` | boolean |  |
| `critical` | boolean |  |
| `defaultTrackEvents` | boolean |  |
| `defaultTtl` | number |  |
| `id` | string |  |
| `key` | string |  |
| `links` | object |  |
| `mobileKey` | string |  |
| `name` | string |  |
| `requireComments` | boolean |  |
| `resourceApprovalSettings` | object |  |
| `secureMode` | boolean |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native LaunchDarkly API, this operation is `PATCH /projects/:projectKey/environments/:environmentKey` (base URL `https://app.launchdarkly.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-environment.md) for the provider-specific parameters and requirements.

