# EasyPost: Get Customs Item

Retrieves details for a customs item from EasyPost.

```
GET https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-customs-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-customs-item?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-customs-item?${params}`, {
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
| `id` | string | yes | EasyPost CustomsItem ID, beginning with cstitem_. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "hsTariffNumber": "string",
      "id": "string",
      "mode": "string",
      "object": "string",
      "originCountry": "string",
      "quantity": 1,
      "value": "string",
      "weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `hsTariffNumber` | string |  |
| `id` | string |  |
| `mode` | string |  |
| `object` | string |  |
| `originCountry` | string |  |
| `quantity` | number |  |
| `value` | string |  |
| `weight` | number |  |

## Native endpoint

Through the native EasyPost API, this operation is `GET /customs_items/:id` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customs-item.md) for the provider-specific parameters and requirements.

