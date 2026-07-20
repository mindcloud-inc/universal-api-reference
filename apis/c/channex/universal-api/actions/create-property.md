# Channex: Create Property

Creates a new property in Channex.

```
POST https://connect.mindcloud.co/v1/universal/channex/latest/actions/create-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/channex/latest/actions/create-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "property": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channex/latest/actions/create-property', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "property": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `property` | object | yes | Top-level property payload object documented by Channex for property creation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "city": "string",
          "country": "string",
          "currency": "string",
          "is_active": true,
          "title": "string"
        },
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.attributes.city` | string |  |
| `data.attributes.country` | string |  |
| `data.attributes.currency` | string |  |
| `data.attributes.is_active` | boolean |  |
| `data.attributes.title` | string |  |
| `data.id` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native Channex API, this operation is `POST /properties` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-property.md) for the provider-specific parameters and requirements.

