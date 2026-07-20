# Ontraport: Retrieve Product Collection Info

Retrieves collection info for products in Ontraport.

```
GET https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/retrieve-product-collection-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ontraport `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/retrieve-product-collection-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/retrieve-product-collection-info?${params}`, {
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
| `search` | string | no | Search the collection info response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cardViewSettings": {},
      "count": "string",
      "listFields": [
        "string"
      ],
      "listFieldSettings": [
        {}
      ],
      "viewMode": "string",
      "widgetSettings": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cardViewSettings` | object |  |
| `count` | string |  |
| `listFields` | array<string> |  |
| `listFieldSettings` | array<object> |  |
| `viewMode` | string |  |
| `widgetSettings` | object |  |

## Native endpoint

Through the native Ontraport API, this operation is `GET /Products/getInfo` (base URL `https://api.ontraport.com/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-product-collection-info.md) for the provider-specific parameters and requirements.

