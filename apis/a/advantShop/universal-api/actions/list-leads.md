# AdvantShop: List Leads

Retrieves leads from AdvantShop.

```
GET https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/list-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AdvantShop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/list-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/list-leads?${params}`, {
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
| `page` | number | no | Page number. AdvantShop defaults to 1. Default: `1`. |
| `itemsPerPage` | number | no | Number of leads per page. AdvantShop defaults to 100. Default: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDate": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "email": "ava@example.com",
      "id": 1,
      "phone": "string",
      "sum": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDate` | date |  |
| `description` | string |  |
| `email` | string |  |
| `id` | number |  |
| `phone` | string |  |
| `sum` | number |  |
| `title` | string |  |

## Native endpoint

Through the native AdvantShop API, this operation is `POST /leads/getlist` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-leads.md) for the provider-specific parameters and requirements.

