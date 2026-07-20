# Contentful: Get entry references



```
GET https://connect.mindcloud.co/v1/universal/contentful/latest/actions/get-entry-references
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Contentful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentful/latest/actions/get-entry-references?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentful/latest/actions/get-entry-references?${params}`, {
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
| `entryId` | string | no |  |
| `environmentId` | string | no |  |
| `include` | string | no |  |
| `spaceId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "sys": {
            "id": "string",
            "type": "string"
          }
        }
      ],
      "limit": 1,
      "skip": 1,
      "sys": {
        "type": "string"
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].sys.id` | string |  |
| `items[].sys.type` | string |  |
| `limit` | number |  |
| `skip` | number |  |
| `sys.type` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Contentful API, this operation is `GET /spaces/:spaceId/environments/:environmentId/entries/:entryId/references` (base URL `https://api.contentful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-entry-references.md) for the provider-specific parameters and requirements.

