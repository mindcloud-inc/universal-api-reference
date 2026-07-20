# Ninetailed: Get Content Type



```
GET https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/get-content-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninetailed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/get-content-type?connectionId=$CONNECTION_ID&spaceId=string&environmentId=string&contentTypeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "string",
  "environmentId": "string",
  "contentTypeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/get-content-type?${params}`, {
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
| `spaceId` | string | yes | Contentful space ID. |
| `environmentId` | string | yes | Contentful environment ID. |
| `contentTypeId` | string | yes | Contentful content type ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "displayField": "string",
      "fields": [
        {}
      ],
      "name": "Ava Chen",
      "sys": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `displayField` | string |  |
| `fields` | array<object> |  |
| `name` | string |  |
| `sys` | object |  |

## Native endpoint

Through the native Ninetailed API, this operation is `GET /spaces/:space_id/environments/:environment_id/content_types/:content_type_id` (base URL `https://api.contentful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-content-type.md) for the provider-specific parameters and requirements.

