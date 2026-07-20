# Swell: Get Variant



```
GET https://connect.mindcloud.co/v1/universal/swell/latest/actions/get-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swell/latest/actions/get-variant?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swell/latest/actions/get-variant?${params}`, {
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
| `id` | string | yes | The Swell variant ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "currency": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "parentId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `currency` | string |  |
| `dateCreated` | date |  |
| `id` | string |  |
| `name` | string |  |
| `parentId` | string |  |

## Native endpoint

Through the native Swell API, this operation is `GET /products\:variants/:id` (base URL `https://api.swell.store`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-variant.md) for the provider-specific parameters and requirements.

