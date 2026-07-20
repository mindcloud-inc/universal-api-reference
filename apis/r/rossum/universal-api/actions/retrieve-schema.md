# Rossum: Retrieve Schema

Retrieves a schema from Rossum.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-schema?connectionId=$CONNECTION_ID&schemaID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "schemaID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-schema?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `schemaID` | number | yes | ID of the schema to retrieve. |

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

Through the native Rossum API, this operation is `GET /schemas/:schemaID` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-schema.md) for the provider-specific parameters and requirements.

