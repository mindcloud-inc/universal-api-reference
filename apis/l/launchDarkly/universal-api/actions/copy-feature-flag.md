# LaunchDarkly: Copy Feature Flag

Copies feature flag settings between LaunchDarkly environments.

```
POST https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/copy-feature-flag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchDarkly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/copy-feature-flag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "featureFlagKey": "string",
  "projectKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/copy-feature-flag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "featureFlagKey": "string",
    "projectKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `featureFlagKey` | string | yes | The LaunchDarkly feature flag key. |
| `projectKey` | string | yes | The LaunchDarkly project key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "clientSideAvailability": {},
      "creationDate": 1,
      "customProperties": {},
      "defaults": {},
      "deprecated": true,
      "description": "string",
      "environments": {},
      "experiments": {},
      "goalIds": [
        "string"
      ],
      "includeInSnippet": true,
      "key": "string",
      "kind": "string",
      "links": {},
      "name": "Ava Chen",
      "tags": [
        "string"
      ],
      "temporary": true,
      "variations": [
        {}
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
| `archived` | boolean |  |
| `clientSideAvailability` | object |  |
| `creationDate` | number |  |
| `customProperties` | object |  |
| `defaults` | object |  |
| `deprecated` | boolean |  |
| `description` | string |  |
| `environments` | object |  |
| `experiments` | object |  |
| `goalIds` | array<string> |  |
| `includeInSnippet` | boolean |  |
| `key` | string |  |
| `kind` | string |  |
| `links` | object |  |
| `name` | string |  |
| `tags` | array<string> |  |
| `temporary` | boolean |  |
| `variations` | array<object> |  |
| `version` | number |  |

## Native endpoint

Through the native LaunchDarkly API, this operation is `POST /flags/:projectKey/:featureFlagKey/copy` (base URL `https://app.launchdarkly.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-feature-flag.md) for the provider-specific parameters and requirements.

