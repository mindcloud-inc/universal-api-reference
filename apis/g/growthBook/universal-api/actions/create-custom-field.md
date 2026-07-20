# GrowthBook: Create a single customField

Creates a new custom field in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/create-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/create-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7",
  "name": "sample",
  "type": "sample",
  "required": "true",
  "sections": [
    "sample"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/create-custom-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "prj_19g6smo332up7",
    "name": "sample",
    "type": "sample",
    "required": "true",
    "sections": ["sample"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The unique key for the custom field Default: `prj_19g6smo332up7`. |
| `name` | string | yes | The display name of the custom field Default: `sample`. |
| `description` | string | no |  |
| `placeholder` | string | no |  |
| `defaultValue` | string | no |  |
| `type` | string | yes | The type of value this custom field will take Default: `sample`. |
| `values` | string | no |  |
| `required` | boolean | yes | Default: `true`. |
| `projects` | list<string> | no |  |
| `sections` | list<string> | yes | What types of objects this custom field is applicable to (feature, experiment) Default: `["sample"]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customField": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customField` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /custom-fields` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-field.md) for the provider-specific parameters and requirements.

