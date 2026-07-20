# Paystack: Fetch Page



```
GET https://connect.mindcloud.co/v1/universal/paystack/latest/actions/fetch-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paystack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/fetch-page?connectionId=$CONNECTION_ID&pageIdOrSlug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageIdOrSlug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paystack/latest/actions/fetch-page?${params}`, {
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
| `pageIdOrSlug` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "amount": 1,
      "createdAt": "string",
      "currency": "string",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "published": true,
      "slug": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `amount` | number |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `published` | boolean |  |
| `slug` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Paystack API, this operation is `GET /page/:pageIdOrSlug` (base URL `https://api.paystack.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-page.md) for the provider-specific parameters and requirements.

