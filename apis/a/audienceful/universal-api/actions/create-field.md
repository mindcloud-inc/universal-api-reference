# Audienceful: Create Field

Creates a new custom field in Audienceful.

```
POST https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/create-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Audienceful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/create-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "dataName": "Ava Chen",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/create-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "dataName": "Ava Chen",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Human-readable field name. |
| `dataName` | string | yes | Field key used in person payloads. |
| `type` | string | yes | Field data type. |
| `editable` | boolean | no | Whether the field can be edited. |
| `required` | boolean | no | Whether the field is required. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataName": "Ava Chen",
      "editable": true,
      "id": "string",
      "internal": true,
      "name": "Ava Chen",
      "required": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataName` | string |  |
| `editable` | boolean |  |
| `id` | string |  |
| `internal` | boolean |  |
| `name` | string |  |
| `required` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Audienceful API, this operation is `POST /people/fields/` (base URL `https://app.audienceful.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-field.md) for the provider-specific parameters and requirements.

