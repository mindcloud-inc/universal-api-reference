# GrowthBook: Partially update a feature

Updates an existing feature in GrowthBook.

```
PUT https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-feature
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-feature" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-feature', {
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
| `description` | string | no | Description of the feature |
| `archived` | boolean | no |  |
| `project` | string | no | An associated project ID |
| `owner` | string | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `defaultValue` | string | no |  |
| `tags` | list<string> | no | List of associated tags. Will override tags completely with submitted list |
| `environments` | object | no |  |
| `prerequisites` | list<string> | no | Feature IDs. Each feature must evaluate to `true` |
| `jsonSchema` | string | no | Use JSON schema to validate the payload of a JSON-type feature value (enterprise only). |
| `customFields` | object | no |  |
| `holdout` | object | no |  |

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

Through the native GrowthBook API, this operation is `POST /features/:id` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-feature.md) for the provider-specific parameters and requirements.

