# Rossum: Create Schema

Creates a new schema in Rossum.

```
POST https://connect.mindcloud.co/v1/universal/rossum/latest/actions/create-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/create-schema" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "content": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rossum/latest/actions/create-schema', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "content": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the schema to create. |
| `content` | list<object> | yes | Schema content array describing the Rossum sections and datapoints. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        {
          "category": "string",
          "children": [
            {
              "category": "string",
              "constraints": {
                "required": true
              },
              "defaultValue": {},
              "id": "string",
              "label": "string",
              "type": "string",
              "uiConfiguration": {
                "edit": "string",
                "type": "string"
              }
            }
          ],
          "icon": {},
          "id": "string",
          "label": "string"
        }
      ],
      "id": 1,
      "modifiedAt": "string",
      "modifiedBy": "string",
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content[].category` | string |  |
| `content[].children[].category` | string |  |
| `content[].children[].constraints.required` | boolean |  |
| `content[].children[].defaultValue` | object |  |
| `content[].children[].id` | string |  |
| `content[].children[].label` | string |  |
| `content[].children[].type` | string |  |
| `content[].children[].uiConfiguration.edit` | string |  |
| `content[].children[].uiConfiguration.type` | string |  |
| `content[].icon` | object |  |
| `content[].id` | string |  |
| `content[].label` | string |  |
| `id` | number |  |
| `modifiedAt` | string |  |
| `modifiedBy` | string |  |
| `name` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Rossum API, this operation is `POST /schemas` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-schema.md) for the provider-specific parameters and requirements.

