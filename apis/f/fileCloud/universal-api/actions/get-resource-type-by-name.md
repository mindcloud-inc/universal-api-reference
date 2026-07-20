# FileCloud: Get Resource Type by Name

Retrieves a resource type from FileCloud by name.

```
GET https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/get-resource-type-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FileCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/get-resource-type-by-name?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/get-resource-type-by-name?${params}`, {
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
| `name` | string | yes | Resource type name. Verified values include User and Group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "endpoint": "string",
      "id": "string",
      "meta": {},
      "name": "Ava Chen",
      "schema": "string",
      "schemaExtensions": [
        {}
      ],
      "schemas": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `endpoint` | string |  |
| `id` | string |  |
| `meta` | object |  |
| `name` | string |  |
| `schema` | string |  |
| `schemaExtensions` | array<object> |  |
| `schemas` | array<string> |  |

## Native endpoint

Through the native FileCloud API, this operation is `GET /scim/ResourceTypes/:name` (base URL `https://mindcloud.filecloudtrial.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource-type-by-name.md) for the provider-specific parameters and requirements.

