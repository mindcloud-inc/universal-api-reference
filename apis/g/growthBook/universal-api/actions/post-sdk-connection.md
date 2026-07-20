# GrowthBook: Create a single sdk connection

Creates a new SDK connection in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-sdk-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-sdk-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "sample",
  "language": "sample",
  "environment": "production"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-sdk-connection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "sample",
    "language": "sample",
    "environment": "production"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Default: `sample`. |
| `language` | string | yes | Default: `sample`. |
| `sdkVersion` | string | no |  |
| `environment` | string | yes | Default: `production`. |
| `projects` | list<string> | no |  |
| `encryptPayload` | boolean | no |  |
| `includeVisualExperiments` | boolean | no |  |
| `includeDraftExperiments` | boolean | no |  |
| `includeExperimentNames` | boolean | no |  |
| `includeRedirectExperiments` | boolean | no |  |
| `includeRuleIds` | boolean | no |  |
| `includeProjectIdInMetadata` | boolean | no |  |
| `includeCustomFieldsInMetadata` | boolean | no |  |
| `allowedCustomFieldsInMetadata` | list<string> | no |  |
| `includeTagsInMetadata` | boolean | no |  |
| `proxyEnabled` | boolean | no |  |
| `proxyHost` | string | no |  |
| `hashSecureAttributes` | boolean | no |  |
| `remoteEvalEnabled` | boolean | no |  |
| `savedGroupReferencesEnabled` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sdkConnection": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sdkConnection` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /sdk-connections` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-sdk-connection.md) for the provider-specific parameters and requirements.

