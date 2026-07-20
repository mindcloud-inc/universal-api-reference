# Runway: Control A Character

Creates a character performance task in Runway.

```
POST https://connect.mindcloud.co/v1/universal/runway/latest/actions/control-a-character
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/runway/latest/actions/control-a-character" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "character": {},
  "model": "act_two",
  "reference": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runway/latest/actions/control-a-character', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "character": {},
    "model": "act_two",
    "reference": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `character` | object | yes | Character object with type and uri for the image or video character source. |
| `model` | string | yes | Runway currently requires act_two. Default: `act_two`. |
| `reference` | object | yes | Reference video object containing the performance to apply. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Runway API, this operation is `POST /v1/character_performance` (base URL `https://api.dev.runwayml.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/control-a-character.md) for the provider-specific parameters and requirements.

