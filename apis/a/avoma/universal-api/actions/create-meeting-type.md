# Avoma: Create Meeting Type

Creates a new meeting type in Avoma.

```
POST https://connect.mindcloud.co/v1/universal/avoma/latest/actions/create-meeting-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avoma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/create-meeting-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "label": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avoma/latest/actions/create-meeting-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "label": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `label` | string | yes | Label of the meeting type. |
| `description` | string | no | Description of the meeting type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "label": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `label` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Avoma API, this operation is `POST /v1/meeting_type/` (base URL `https://api.avoma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-meeting-type.md) for the provider-specific parameters and requirements.

