# Edoobox: Get Category

Retrieves details for a category from Edoobox.

```
GET https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/get-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edoobox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/get-category?connectionId=$CONNECTION_ID&categoryId=category_997526bfa43f_7513087706" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "categoryId": "category_997526bfa43f_7513087706"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/get-category?${params}`, {
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
| `categoryId` | string | yes | edoobox category ID. Default: `category_997526bfa43f_7513087706`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archive": true,
      "category": "string",
      "design": "string",
      "id": "string",
      "image": true,
      "internalCode": "string",
      "name": "Ava Chen",
      "order": 1,
      "preventMultipleBookings": true,
      "rowLft": 1,
      "rowRgt": 1,
      "trash": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archive` | boolean |  |
| `category` | string |  |
| `design` | string |  |
| `id` | string |  |
| `image` | boolean |  |
| `internalCode` | string |  |
| `name` | string |  |
| `order` | number |  |
| `preventMultipleBookings` | boolean |  |
| `rowLft` | number |  |
| `rowRgt` | number |  |
| `trash` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Edoobox API, this operation is `GET /category/:category_id` (base URL `https://app2.edoobox.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-category.md) for the provider-specific parameters and requirements.

