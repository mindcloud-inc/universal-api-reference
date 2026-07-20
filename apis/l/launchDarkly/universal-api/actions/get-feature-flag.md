# LaunchDarkly: Get Feature Flag

Retrieves a feature flag from LaunchDarkly.

```
GET https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/get-feature-flag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchDarkly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/get-feature-flag?connectionId=$CONNECTION_ID&featureFlagKey=string&projectKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "featureFlagKey": "string",
  "projectKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/get-feature-flag?${params}`, {
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

Through the native LaunchDarkly API, this operation is `GET /flags/:projectKey/:featureFlagKey` (base URL `https://app.launchdarkly.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feature-flag.md) for the provider-specific parameters and requirements.

