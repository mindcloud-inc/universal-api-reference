# Xola: Retrieve Order Form

Retrieves the form for an order in Xola.

```
GET https://connect.mindcloud.co/v1/universal/xola/latest/actions/retrieve-order-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xola `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xola/latest/actions/retrieve-order-form?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xola/latest/actions/retrieve-order-form?${params}`, {
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
| `id` | string | yes | Order identifier from Xola. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "questions": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Order identifier. |
| `questions[]` | array<object> | Questions included in the order form. |

## Native endpoint

Through the native Xola API, this operation is `GET /orders/{id}/questions` (base URL `https://sandbox.xola.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-order-form.md) for the provider-specific parameters and requirements.

