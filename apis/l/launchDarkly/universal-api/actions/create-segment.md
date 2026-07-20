# LaunchDarkly: Create Segment

Creates a new segment in LaunchDarkly.

```
POST https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/create-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchDarkly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/create-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "environmentKey": "string",
  "projectKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/create-segment', {
  method: 'POST',
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
      "creationDate": 1,
      "deleted": true,
      "description": "string",
      "excluded": [
        "string"
      ],
      "excludedContexts": [
        {}
      ],
      "generation": 1,
      "included": [
        "string"
      ],
      "includedContexts": [
        {}
      ],
      "key": "string",
      "lastModifiedDate": 1,
      "links": {},
      "name": "Ava Chen",
      "rules": [
        {}
      ],
      "tags": [
        "string"
      ],
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | number |  |
| `deleted` | boolean |  |
| `description` | string |  |
| `excluded` | array<string> |  |
| `excludedContexts` | array<object> |  |
| `generation` | number |  |
| `included` | array<string> |  |
| `includedContexts` | array<object> |  |
| `key` | string |  |
| `lastModifiedDate` | number |  |
| `links` | object |  |
| `name` | string |  |
| `rules` | array<object> |  |
| `tags` | array<string> |  |
| `version` | number |  |

## Native endpoint

Through the native LaunchDarkly API, this operation is `POST /segments/:projectKey/:environmentKey` (base URL `https://app.launchdarkly.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-segment.md) for the provider-specific parameters and requirements.

