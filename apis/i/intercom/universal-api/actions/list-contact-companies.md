# Intercom: List Contact Companies



```
GET https://connect.mindcloud.co/v1/universal/intercom/latest/actions/list-contact-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intercom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intercom/latest/actions/list-contact-companies?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intercom/latest/actions/list-contact-companies?${params}`, {
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
| `contactId` | string | yes | Intercom contact identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        "string"
      ],
      "pages": {
        "next": "string",
        "page": 1,
        "perPage": 1,
        "totalPages": 1,
        "type": "string"
      },
      "totalCount": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<string> |  |
| `pages` | object |  |
| `pages.next` | string |  |
| `pages.page` | number |  |
| `pages.perPage` | number |  |
| `pages.totalPages` | number |  |
| `pages.type` | string |  |
| `totalCount` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Intercom API, this operation is `GET /contacts/:contact_id/companies` (base URL `https://api.intercom.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-companies.md) for the provider-specific parameters and requirements.

