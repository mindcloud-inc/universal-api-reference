# ContentStudio: List Workspaces

Retrieves workspaces for the authenticated user from ContentStudio.

```
GET https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContentStudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/list-workspaces?${params}`, {
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
| `page` | number | no | Page number for pagination. |
| `per_page` | number | no | Number of items per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyLogo": "string",
      "companyName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "Id": "string",
      "logo": "string",
      "name": "Ava Chen",
      "onHold": true,
      "policy": {},
      "slug": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyLogo` | string |  |
| `companyName` | string |  |
| `createdAt` | date |  |
| `Id` | string |  |
| `logo` | string |  |
| `name` | string |  |
| `onHold` | boolean |  |
| `policy` | object |  |
| `slug` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native ContentStudio API, this operation is `GET /workspaces` (base URL `https://api.contentstudio.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

