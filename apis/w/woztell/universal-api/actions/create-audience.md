# Woztell: Create Audience

Creates an audience in your Woztell workspace.

```
POST https://connect.mindcloud.co/v1/universal/woztell/latest/actions/create-audience
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Woztell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/woztell/latest/actions/create-audience" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/woztell/latest/actions/create-audience', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.input.name` | string | no | Audience name. |
| `variables.input.description` | string | no | Audience description. |
| `variables.input.static` | boolean | no | Whether the audience is static. |
| `variables.input.tags` | list<string> | no | Tags to assign to the audience. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createAudience": {
          "audience": {
            "_id": "string",
            "channelId": "string",
            "createdAt": 1,
            "description": "string",
            "etag": "string",
            "id": "string",
            "name": "Ava Chen",
            "static": true,
            "updatedAt": 1
          },
          "clientMutationId": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.createAudience.audience._id` | string |  |
| `data.createAudience.audience.channelId` | string |  |
| `data.createAudience.audience.createdAt` | number |  |
| `data.createAudience.audience.description` | string |  |
| `data.createAudience.audience.etag` | string |  |
| `data.createAudience.audience.id` | string |  |
| `data.createAudience.audience.name` | string |  |
| `data.createAudience.audience.static` | boolean |  |
| `data.createAudience.audience.updatedAt` | number |  |
| `data.createAudience.clientMutationId` | string |  |

## Native endpoint

Through the native Woztell API, this operation is `POST /` (base URL `https://open.api.woztell.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-audience.md) for the provider-specific parameters and requirements.

