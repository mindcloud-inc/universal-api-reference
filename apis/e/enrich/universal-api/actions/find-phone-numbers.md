# Enrich.so: Find Phone Numbers

Finds phone numbers in Enrich.so by email or profile URL.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/find-phone-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/find-phone-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/find-phone-numbers?${params}`, {
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
| `email` | string | no | Email address to use for phone lookup. Provide this or LinkedIn. Default: `satyan@microsoft.com`. |
| `linkedin` | string | no | LinkedIn/profile URL to use for phone lookup. Provide this or Email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits_remaining": 1,
      "credits_used": 1,
      "email": "ava@example.com",
      "linkedin": "https://example.com",
      "message": "string",
      "phone": "string",
      "phones": [
        {}
      ],
      "success": true,
      "total_credits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_remaining` | number | Credits remaining for the team. |
| `credits_used` | number | Credits already consumed. |
| `email` | string | Email used for the phone lookup. |
| `linkedin` | string | LinkedIn profile URL associated with the lookup. |
| `message` | string | Provider status message. |
| `phone` | string | Primary phone number returned by the provider. |
| `phones` | array<object> | Phone records returned by the provider. |
| `success` | boolean | Whether the lookup succeeded. |
| `total_credits` | number | Total credits available to the team. |

## Native endpoint

Through the native Enrich.so API, this operation is `GET /reverse-lookup/phones` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-phone-numbers.md) for the provider-specific parameters and requirements.

