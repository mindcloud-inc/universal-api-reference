# Woztell: Update Audience

Updates an audience in your Woztell workspace.

```
PUT https://connect.mindcloud.co/v1/universal/woztell/latest/actions/update-audience
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Woztell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/woztell/latest/actions/update-audience" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.input.audienceId": "string",
  "variables.input.etag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/woztell/latest/actions/update-audience', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.input.audienceId": "string",
    "variables.input.etag": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.input.audienceId` | string | yes | Raw Woztell audience _id to update. |
| `variables.input.etag` | string | yes | Current Woztell audience etag for optimistic concurrency. |
| `variables.input.description` | string | no | Updated audience description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "updateAudience": {
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
| `data.updateAudience.audience._id` | string |  |
| `data.updateAudience.audience.channelId` | string |  |
| `data.updateAudience.audience.createdAt` | number |  |
| `data.updateAudience.audience.description` | string |  |
| `data.updateAudience.audience.etag` | string |  |
| `data.updateAudience.audience.id` | string |  |
| `data.updateAudience.audience.name` | string |  |
| `data.updateAudience.audience.static` | boolean |  |
| `data.updateAudience.audience.updatedAt` | number |  |
| `data.updateAudience.clientMutationId` | string |  |

## Native endpoint

Through the native Woztell API, this operation is `POST /` (base URL `https://open.api.woztell.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-audience.md) for the provider-specific parameters and requirements.

