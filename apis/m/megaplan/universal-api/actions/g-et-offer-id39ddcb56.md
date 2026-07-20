# Megaplan: Get Offer



```
GET https://connect.mindcloud.co/v1/universal/megaplan/latest/actions/g-et-offer-id39ddcb56
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Megaplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/megaplan/latest/actions/g-et-offer-id39ddcb56?connectionId=$CONNECTION_ID&id=string&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/megaplan/latest/actions/g-et-offer-id39ddcb56?${params}`, {
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
| `id` | string | yes | Required path parameter from Megaplan RAML. |
| `id` | number | yes | Id товара, который нужно получить |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "data": {},
      "id": "string",
      "meta": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string | Megaplan object type when present. |
| `data` | object | Megaplan response data. |
| `id` | string | Megaplan entity identifier when present. |
| `meta` | object | Megaplan response metadata. |
| `success` | boolean | Operation success indicator when present. |

## Native endpoint

Through the native Megaplan API, this operation is `GET /offer/:id` (base URL `https://m60888876.megaplan.ru/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/g-et-offer-id39ddcb56.md) for the provider-specific parameters and requirements.

