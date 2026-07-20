# DoneDone: Get Project

Retrieves project details from DoneDone.

```
GET https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DoneDone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/get-project?connectionId=$CONNECTION_ID&accountId=1&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/get-project?${params}`, {
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
| `accountId` | number | yes | DoneDone account ID. |
| `projectId` | number | yes | DoneDone internal project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "isFavorite": true,
      "listPeople": [
        {
          "email": "ava@example.com",
          "id": 1,
          "isGuest": true,
          "name": "Ava Chen",
          "photoUrl": "https://example.com"
        }
      ],
      "name": "Ava Chen",
      "workflow": {
        "description": "string",
        "id": 1,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `isFavorite` | boolean |  |
| `listPeople[].email` | string |  |
| `listPeople[].id` | number |  |
| `listPeople[].isGuest` | boolean |  |
| `listPeople[].name` | string |  |
| `listPeople[].photoUrl` | string |  |
| `name` | string |  |
| `workflow.description` | string |  |
| `workflow.id` | number |  |
| `workflow.name` | string |  |

## Native endpoint

Through the native DoneDone API, this operation is `GET /:account_id/internal-projects/:internal_project_id` (base URL `https://2.donedone.com/public-api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

