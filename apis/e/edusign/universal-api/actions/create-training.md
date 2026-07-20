# Edusign: Create Training

Creates a new training in Edusign.

```
POST https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-training
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-training" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "start": "string",
  "end": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-training', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "start": "string",
    "end": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Training name |
| `start` | string | yes | Start date of the training |
| `end` | string | yes | End date of the training (format YYYY-MM-DD HH:mm:ss, ISO 8601) |
| `goals` | string | no | Training goals |
| `students[]` | array<string> | no |  |
| `apiId` | string | no | The ID of your API resource representing the training |
| `apiType` | string | no | The name of your API from where you created the training |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tags[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `POST /v1/trainings/` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-training.md) for the provider-specific parameters and requirements.

