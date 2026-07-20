# GrowthBook: Update a single sdk connection

Updates an existing SDK connection in GrowthBook.

```
PUT https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/put-sdk-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/put-sdk-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/put-sdk-connection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "prj_19g6smo332up7"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The id of the requested resource Default: `prj_19g6smo332up7`. |
| `name` | string | no |  |
| `language` | string | no |  |
| `sdkVersion` | string | no |  |
| `environment` | string | no |  |
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

Through the native GrowthBook API, this operation is `PUT /sdk-connections/:id` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-sdk-connection.md) for the provider-specific parameters and requirements.

