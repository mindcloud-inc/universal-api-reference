# GrowthBook: Update a single customField

Updates an existing custom field in GrowthBook.

```
PUT https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-custom-field', {
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
| `id` | string | yes | Default: `prj_19g6smo332up7`. |
| `name` | string | no | The display name of the custom field |
| `description` | string | no |  |
| `placeholder` | string | no |  |
| `defaultValue` | string | no |  |
| `values` | string | no |  |
| `required` | boolean | no |  |
| `projects` | list<string> | no |  |
| `sections` | list<string> | no | What types of objects this custom field is applicable to (feature, experiment) |
| `active` | boolean | no |  |

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

Through the native GrowthBook API, this operation is `PUT /custom-fields/:id` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-custom-field.md) for the provider-specific parameters and requirements.

