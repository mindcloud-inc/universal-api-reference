# DONNAJAMES Easy: Update Source Tag

Updates an existing source tag in DONNAJAMES Easy.

```
PUT https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/update-source-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DONNAJAMES Easy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/update-source-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/update-source-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `color` | string | no |  |
| `name` | string | no |  |
| `uuid` | string | yes | Source tag uuid |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "created_at": "string",
      "modified_at": "string",
      "name": "Ava Chen",
      "source_uuids": [
        "string"
      ],
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `created_at` | string |  |
| `modified_at` | string |  |
| `name` | string |  |
| `source_uuids` | array<string> |  |
| `uuid` | string |  |

## Native endpoint

Through the native DONNAJAMES Easy API, this operation is `POST source-tag/:uuid/update` (base URL `https://app.gpt-trainer.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-source-tag.md) for the provider-specific parameters and requirements.

