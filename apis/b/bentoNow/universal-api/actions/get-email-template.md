# Bento Now: Get Email Template

Retrieves an email template with stats from Bento Now.

```
GET https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/get-email-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bento Now `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/get-email-template?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/get-email-template?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "html": "string",
        "name": "Ava Chen",
        "stats": {},
        "subject": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.createdAt` | date |  |
| `attributes.html` | string |  |
| `attributes.name` | string |  |
| `attributes.stats` | object |  |
| `attributes.subject` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Bento Now API, this operation is `GET /v1/fetch/emails/templates/:id` (base URL `https://app.bentonow.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-template.md) for the provider-specific parameters and requirements.

