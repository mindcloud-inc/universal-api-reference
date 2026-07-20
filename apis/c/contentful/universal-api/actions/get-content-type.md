# Contentful: Get content type



```
GET https://connect.mindcloud.co/v1/universal/contentful/latest/actions/get-content-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Contentful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentful/latest/actions/get-content-type?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentful/latest/actions/get-content-type?${params}`, {
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
| `contentTypeId` | string | no |  |
| `environmentId` | string | no |  |
| `spaceId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "displayField": "string",
      "fields": [
        {
          "id": "string",
          "name": "Ava Chen",
          "type": "string"
        }
      ],
      "name": "Ava Chen",
      "sys": {
        "id": "string",
        "type": "string",
        "version": 1
      }
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
| `fields[].id` | string |  |
| `fields[].name` | string |  |
| `fields[].type` | string |  |
| `name` | string |  |
| `sys.id` | string |  |
| `sys.type` | string |  |
| `sys.version` | number |  |

## Native endpoint

Through the native Contentful API, this operation is `GET /spaces/:spaceId/environments/:environmentId/content_types/:contentTypeId` (base URL `https://api.contentful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-content-type.md) for the provider-specific parameters and requirements.

