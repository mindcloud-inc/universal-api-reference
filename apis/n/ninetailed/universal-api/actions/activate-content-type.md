# Ninetailed: Activate Content Type



```
PUT https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/activate-content-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninetailed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/activate-content-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string",
  "environmentId": "string",
  "contentTypeId": "string",
  "contentfulVersion": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/activate-content-type', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string",
    "environmentId": "string",
    "contentTypeId": "string",
    "contentfulVersion": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spaceId` | string | yes | Contentful space ID. |
| `environmentId` | string | yes | Contentful environment ID. |
| `contentTypeId` | string | yes | Contentful content type ID. |
| `contentfulVersion` | number | yes | Current content type version to send as X-Contentful-Version. |

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

Through the native Ninetailed API, this operation is `PUT /spaces/:space_id/environments/:environment_id/content_types/:content_type_id/published` (base URL `https://api.contentful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/activate-content-type.md) for the provider-specific parameters and requirements.

