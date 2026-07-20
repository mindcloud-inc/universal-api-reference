# Saleshandy: Search DNC Items



```
GET https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/search-dnc-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Saleshandy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/search-dnc-items?connectionId=$CONNECTION_ID&limit=25&offset=0&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/search-dnc-items?${params}`, {
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
| `search` | string | no | Optional DNC item search string. |
| `type` | string | yes | DNC item type to search for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "payload": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `payload` | object |  |

## Native endpoint

Through the native Saleshandy API, this operation is `GET /dnc/item/search` (base URL `https://open-api.saleshandy.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-dnc-items.md) for the provider-specific parameters and requirements.

