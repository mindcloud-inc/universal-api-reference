# Xola: Retrieve Demographic

Retrieves a demographic from Xola by ID.

```
GET https://connect.mindcloud.co/v1/universal/xola/latest/actions/retrieve-demographic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xola `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xola/latest/actions/retrieve-demographic?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xola/latest/actions/retrieve-demographic?${params}`, {
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
| `id` | string | yes | Demographic identifier from Xola. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "discount": {
        "amount": 1,
        "amountType": "string"
      },
      "experience": {
        "id": "string"
      },
      "id": "string",
      "label": "string",
      "labelCanonical": "string",
      "object": "string",
      "parent": {
        "id": "string"
      },
      "seller": {
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `discount.amount` | number | Discount amount. |
| `discount.amountType` | string | Discount amount type. |
| `experience.id` | string | Associated experience identifier. |
| `id` | string | Demographic identifier. |
| `label` | string | Display label. |
| `labelCanonical` | string | Canonical label. |
| `object` | string | Xola object type. |
| `parent.id` | string | Parent demographic identifier. |
| `seller.id` | string | Owning seller identifier. |

## Native endpoint

Through the native Xola API, this operation is `GET /demographics/{id}` (base URL `https://sandbox.xola.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-demographic.md) for the provider-specific parameters and requirements.

