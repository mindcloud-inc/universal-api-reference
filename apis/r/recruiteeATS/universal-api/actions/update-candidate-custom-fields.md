# Recruitee ATS: Update Candidate Custom Fields



```
PUT https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/update-candidate-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recruitee ATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/update-candidate-custom-fields" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "field.name": "Ava Chen",
  "field.kind": "single_line",
  "field.values": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/update-candidate-custom-fields', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "field.name": "Ava Chen",
    "field.kind": "single_line",
    "field.values": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Candidate ID. |
| `field.name` | string | yes | Profile field name. |
| `field.values` | list<object> | yes | Array of profile field value objects. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `field.kind` | string | yes | Profile field kind. Default: `single_line`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field": {
        "fixed": {},
        "id": 1,
        "kind": "string",
        "name": "Ava Chen",
        "origin": "string",
        "values": [
          {
            "text": "string"
          }
        ],
        "visibility": {
          "level": "string"
        },
        "visible": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field.fixed` | object |  |
| `field.id` | number |  |
| `field.kind` | string |  |
| `field.name` | string |  |
| `field.origin` | string |  |
| `field.values[].text` | string |  |
| `field.visibility.level` | string |  |
| `field.visible` | boolean |  |

## Native endpoint

Through the native Recruitee ATS API, this operation is `POST /c/:company_id/custom_fields/candidates/:id/fields` (base URL `https://api.recruitee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-candidate-custom-fields.md) for the provider-specific parameters and requirements.

