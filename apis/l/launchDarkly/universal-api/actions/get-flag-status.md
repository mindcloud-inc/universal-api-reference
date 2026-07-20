# LaunchDarkly: Get Flag Status

Retrieves a feature flag status across LaunchDarkly environments.

```
GET https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/get-flag-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchDarkly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/get-flag-status?connectionId=$CONNECTION_ID&featureFlagKey=string&projectKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "featureFlagKey": "string",
  "projectKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/get-flag-status?${params}`, {
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
      "environments": {},
      "key": "string",
      "links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `environments` | object |  |
| `key` | string |  |
| `links` | object |  |

## Native endpoint

Through the native LaunchDarkly API, this operation is `GET /flag-status/:projectKey/:featureFlagKey` (base URL `https://app.launchdarkly.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-flag-status.md) for the provider-specific parameters and requirements.

