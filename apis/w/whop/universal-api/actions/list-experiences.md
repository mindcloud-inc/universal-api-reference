# Whop: List Experiences

Retrieves experiences from Whop for a company.

```
GET https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-experiences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-experiences?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-experiences?${params}`, {
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
| `companyId` | string | yes | The unique identifier of the company to list experiences for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "app": {
        "icon": {
          "url": "https://example.com"
        },
        "id": "string",
        "name": "Ava Chen"
      },
      "company": {
        "id": "string",
        "route": "string",
        "title": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isPublic": true,
      "name": "Ava Chen",
      "order": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app` | object |  |
| `app.icon` | object |  |
| `app.icon.url` | string |  |
| `app.id` | string |  |
| `app.name` | string |  |
| `company` | object |  |
| `company.id` | string |  |
| `company.route` | string |  |
| `company.title` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `isPublic` | boolean |  |
| `name` | string |  |
| `order` | string |  |

## Native endpoint

Through the native Whop API, this operation is `GET /api/v1/experiences` (base URL `https://api.whop.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-experiences.md) for the provider-specific parameters and requirements.

