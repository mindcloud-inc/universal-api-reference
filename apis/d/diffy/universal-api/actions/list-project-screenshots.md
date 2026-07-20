# Diffy: List Project Screenshots

Retrieves screenshots for a project from Diffy.

```
GET https://connect.mindcloud.co/v1/universal/diffy/latest/actions/list-project-screenshots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diffy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffy/latest/actions/list-project-screenshots?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diffy/latest/actions/list-project-screenshots?${params}`, {
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
| `id` | number | yes | Project ID. |
| `page` | number | no | Page number, starting at 0. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "development": "string",
      "hasBaseline": true,
      "numberItemsOnPage": 1,
      "production": "string",
      "projectName": "Ava Chen",
      "screenshots": [
        {}
      ],
      "staging": "string",
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `development` | string | Development base URL. |
| `hasBaseline` | boolean | Whether the screenshot list includes baseline screenshots. |
| `numberItemsOnPage` | number | Number of items on the returned page. |
| `production` | string | Production base URL. |
| `projectName` | string | Project name. |
| `screenshots` | array<object> | Project screenshots on the selected page. |
| `staging` | string | Staging base URL. |
| `totalPages` | number | Total screenshot pages. |

## Native endpoint

Through the native Diffy API, this operation is `GET /projects/:id/screenshots` (base URL `https://app.diffy.website/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-screenshots.md) for the provider-specific parameters and requirements.

