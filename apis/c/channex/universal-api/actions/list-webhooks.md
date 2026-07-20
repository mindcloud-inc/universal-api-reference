# Channex: List Webhooks

Retrieves webhooks from your Channex account.

```
GET https://connect.mindcloud.co/v1/universal/channex/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channex/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channex/latest/actions/list-webhooks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "attributes": {
            "callback_url": "https://example.com",
            "event_mask": "string",
            "is_active": true,
            "send_data": true
          },
          "id": "string",
          "relationships": {
            "property": {
              "data": {
                "id": "string"
              }
            }
          },
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].attributes.callback_url` | string |  |
| `data[].attributes.event_mask` | string |  |
| `data[].attributes.is_active` | boolean |  |
| `data[].attributes.send_data` | boolean |  |
| `data[].id` | string |  |
| `data[].relationships.property.data.id` | string |  |
| `data[].type` | string |  |

## Native endpoint

Through the native Channex API, this operation is `GET /webhooks` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

