# Bokun: Get Resource

Retrieves a resource by ID from Bokun.

```
GET https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bokun `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-resource?connectionId=$CONNECTION_ID&resourceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-resource?${params}`, {
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
| `resourceId` | number | yes | The Bokun resource ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capacity": 1,
      "created": 1,
      "id": 1,
      "lastModified": 1,
      "resourcePoolIds": [
        1
      ],
      "title": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capacity` | number |  |
| `created` | number |  |
| `id` | number |  |
| `lastModified` | number |  |
| `resourcePoolIds` | array<number> |  |
| `title` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Bokun API, this operation is `GET /restapi/v2.0/resource/:resourceId` (base URL `https://api.bokun.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource.md) for the provider-specific parameters and requirements.

