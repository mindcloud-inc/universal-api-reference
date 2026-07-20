# Sakari SMS: Get Lead Form Conversion Data

Retrieves lead form conversion data from Sakari SMS.

```
GET https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/get-lead-form-conversion-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sakari SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/get-lead-form-conversion-data?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/get-lead-form-conversion-data?${params}`, {
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
| `formId` | string | yes |  |
| `start` | string | no | General search term that specifies start date |
| `end` | string | no | General search term that specifies end date |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "country": "string",
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "mobile": "string"
      },
      "id": "string",
      "ip": "string",
      "pageUrl": "https://example.com",
      "submitted": "2026-05-07T12:00:00.000Z",
      "submittedFields": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | object |  |
| `contact.country` | string |  |
| `contact.email` | string |  |
| `contact.firstName` | string |  |
| `contact.id` | string |  |
| `contact.lastName` | string |  |
| `contact.mobile` | string |  |
| `id` | string |  |
| `ip` | string |  |
| `pageUrl` | string |  |
| `submitted` | date |  |
| `submittedFields` | string |  |

## Native endpoint

Through the native Sakari SMS API, this operation is `GET /v1/accounts/:accountId/forms/:formId/conversions` (base URL `https://api.sakari.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead-form-conversion-data.md) for the provider-specific parameters and requirements.

