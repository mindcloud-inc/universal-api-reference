# Stripo: Get Email

Retrieves an email from Stripo.

```
GET https://connect.mindcloud.co/v1/universal/stripo/latest/actions/get-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripo/latest/actions/get-email?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripo/latest/actions/get-email?${params}`, {
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
| `id` | number | yes | The email ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "css": "string",
      "html": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `css` | string | Email CSS returned by Stripo when included in the detail payload. |
| `html` | string | Email HTML returned by Stripo when included in the detail payload. |
| `id` | number | Email ID. |
| `name` | string | Email name. |

## Native endpoint

Through the native Stripo API, this operation is `GET /emails/:id` (base URL `https://my.stripo.email/emailgeneration/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email.md) for the provider-specific parameters and requirements.

