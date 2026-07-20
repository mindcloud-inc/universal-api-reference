# Bokun: Get Resource Pool

Retrieves a resource pool by ID from Bokun.

```
GET https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-resource-pool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bokun `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-resource-pool?connectionId=$CONNECTION_ID&resourcePoolId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourcePoolId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-resource-pool?${params}`, {
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
| `resourcePoolId` | number | yes | The Bokun resource pool ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "id": 1,
      "lastModified": 1,
      "links": [
        {}
      ],
      "resourceIds": [
        1
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `id` | number |  |
| `lastModified` | number |  |
| `links` | array<object> |  |
| `resourceIds` | array<number> |  |
| `title` | string |  |

## Native endpoint

Through the native Bokun API, this operation is `GET /restapi/v2.0/resource/pool/:resourcePoolId` (base URL `https://api.bokun.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource-pool.md) for the provider-specific parameters and requirements.

