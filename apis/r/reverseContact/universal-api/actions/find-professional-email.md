# Reverse Contact: Find Professional Email



```
GET https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/find-professional-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reverse Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/find-professional-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/find-professional-email?${params}`, {
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
| `url` | string | no | Social profile URL to use for email discovery. |
| `firstName` | string | no | Person first name for name-and-company lookup. |
| `lastName` | string | no | Person last name for name-and-company lookup. |
| `fullName` | string | no | Full name alternative to first and last name. |
| `companyDomain` | string | no | Company domain for name-and-company lookup. |
| `webhookUrl` | string | no | HTTPS callback URL for async results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alternatives": [
        "string"
      ],
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "validation": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alternatives[]` | string |  |
| `email` | string |  |
| `full_name` | string |  |
| `validation` | string |  |

## Native endpoint

Through the native Reverse Contact API, this operation is `POST /v2/contact/email` (base URL `https://api.reversecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-professional-email.md) for the provider-specific parameters and requirements.

