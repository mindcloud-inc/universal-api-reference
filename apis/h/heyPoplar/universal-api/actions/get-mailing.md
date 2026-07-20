# HeyPoplar: Get Mailing

Retrieves a mailing from HeyPoplar.

```
GET https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/get-mailing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HeyPoplar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/get-mailing?connectionId=$CONNECTION_ID&mailingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/get-mailing?${params}`, {
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
| `mailingId` | string | yes | ID of the mailing to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "back_url": "https://example.com",
      "creative_id": "string",
      "front_url": "https://example.com",
      "id": "string",
      "pdf_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `back_url` | string | Public URL to the back preview image from the official Poplar mailing response example. |
| `creative_id` | string | Creative identifier from the official Poplar mailing response example. |
| `front_url` | string | Public URL to the front preview image from the official Poplar mailing response example. |
| `id` | string | Mailer identifier from the official Poplar mailing response example. |
| `pdf_url` | string | Public URL to the PDF preview from the official Poplar mailing response example. |

## Native endpoint

Through the native HeyPoplar API, this operation is `GET /mailing/:mailing_id` (base URL `https://api.heypoplar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mailing.md) for the provider-specific parameters and requirements.

