# GrowthBook: Create a single feature

Creates a new feature in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-feature
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-feature" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7",
  "owner": "sample",
  "valueType": "sample",
  "defaultValue": "sample"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-feature', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "prj_19g6smo332up7",
    "owner": "sample",
    "valueType": "sample",
    "defaultValue": "sample"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | A unique key name for the feature. Feature keys can only include letters, numbers, hyphens, and underscores. Default: `prj_19g6smo332up7`. |
| `archived` | boolean | no |  |
| `description` | string | no | Description of the feature |
| `owner` | string | yes | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. Default: `sample`. |
| `project` | string | no | An associated project ID |
| `valueType` | string | yes | The data type of the feature payload. Boolean by default. Default: `sample`. |
| `defaultValue` | string | yes | Default value when feature is enabled. Type must match `valueType`. Default: `sample`. |
| `tags` | list<string> | no | List of associated tags |
| `environments` | object | no | A dictionary of environments that are enabled for this feature. Keys supply the names of environments. Environments belong to organization and are not specified will be disabled by default. |
| `prerequisites` | list<string> | no | Feature IDs. Each feature must evaluate to `true` |
| `jsonSchema` | string | no | Use JSON schema to validate the payload of a JSON-type feature value (enterprise only). |
| `customFields` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "feature": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `feature` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /features` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-feature.md) for the provider-specific parameters and requirements.

