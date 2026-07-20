# imgix: Update Source

Updates a source in imgix.

```
PUT https://connect.mindcloud.co/v1/universal/imgix/latest/actions/update-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a imgix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/imgix/latest/actions/update-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceId": "69de49d580720625c04f9162"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/imgix/latest/actions/update-source', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceId": "69de49d580720625c04f9162"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceId` | string | yes | The imgix source_id. Default: `69de49d580720625c04f9162`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "deployment": {
            "type": "string"
          },
          "deploymentStatus": "string",
          "enabled": true,
          "name": "Ava Chen"
        },
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.attributes.deployment.type` | string |  |
| `data.attributes.deploymentStatus` | string |  |
| `data.attributes.enabled` | boolean |  |
| `data.attributes.name` | string |  |
| `data.id` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native imgix API, this operation is `PATCH sources/:sourceId` (base URL `https://api.imgix.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-source.md) for the provider-specific parameters and requirements.

