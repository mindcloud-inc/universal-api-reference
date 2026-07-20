# Infobip: Get Email Templates



```
GET https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-email-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-email-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-email-templates?${params}`, {
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
| `page` | number | no | Identifies a specific page number from which to retrieve the email template details. |
| `size` | number | no | Identifies the maximum number of email templates returned in the list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "paging": {
        "page": 1,
        "size": 1,
        "totalPages": 1,
        "totalResults": 1
      },
      "results": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "imagePreviewUrl": "https://example.com",
        "name": "Ava Chen",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `paging` | object |  |
| `paging.page` | number |  |
| `paging.size` | number |  |
| `paging.totalPages` | number |  |
| `paging.totalResults` | number |  |
| `results` | array<object> |  |
| `results.createdAt` | date |  |
| `results.id` | number |  |
| `results.imagePreviewUrl` | string |  |
| `results.name` | string |  |
| `results.updatedAt` | date |  |

## Native endpoint

Through the native Infobip API, this operation is `GET /email/1/templates` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-templates.md) for the provider-specific parameters and requirements.

