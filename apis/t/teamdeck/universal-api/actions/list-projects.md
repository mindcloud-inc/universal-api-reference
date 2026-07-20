# Teamdeck: List Projects

Retrieves projects from your Teamdeck organization.

```
GET https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamdeck `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/list-projects?${params}`, {
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
| `fields` | string | no |  |
| `expand` | string | no |  |
| `name` | string | no |  |
| `archived` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "color": "string",
      "createdAt": "string",
      "defaultApproverId": 1,
      "enableTimeEntryApproval": 1,
      "id": 1,
      "name": "Ava Chen",
      "organizationUnitId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `color` | string |  |
| `createdAt` | string |  |
| `defaultApproverId` | number |  |
| `enableTimeEntryApproval` | number |  |
| `id` | number |  |
| `name` | string |  |
| `organizationUnitId` | number |  |

## Native endpoint

Through the native Teamdeck API, this operation is `GET /projects` (base URL `https://api.teamdeck.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

