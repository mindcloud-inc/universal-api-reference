# Podio: Get Item Values v2

Retrieves item values from Podio.

```
GET https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-item-values-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-item-values-v2?connectionId=$CONNECTION_ID&itemId=123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-item-values-v2?${params}`, {
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
| `itemId` | number | yes | The id of the item. Example: `123456789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": {},
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | object |  |
| `title` | string |  |

## Native endpoint

Through the native Podio API, this operation is `GET /item/:item_id/value/v2` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item-values-v2.md) for the provider-specific parameters and requirements.

