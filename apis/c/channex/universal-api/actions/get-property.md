# Channex: Get Property

Retrieves an existing property from Channex.

```
GET https://connect.mindcloud.co/v1/universal/channex/latest/actions/get-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channex/latest/actions/get-property?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channex/latest/actions/get-property?${params}`, {
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
| `id` | string | yes | UUID of the property to retrieve. |

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

Through the native Channex API, this operation is `GET /properties/:id` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-property.md) for the provider-specific parameters and requirements.

