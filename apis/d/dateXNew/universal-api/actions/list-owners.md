# DateX: List Owners



```
GET https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/list-owners
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/list-owners?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/list-owners?${params}`, {
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
| `filters.lookups[]` | array<string> | no | Owner lookup filters. |
| `filters.names[]` | array<string> | no | Owner name filters. |
| `filters.statuses[]` | array<string> | no | Owner status filters. |
| `filters.project.lookups[]` | array<string> | no | Project lookup filters. |
| `filters.project.names[]` | array<string> | no | Project name filters. |
| `filters.project.statuses[]` | array<string> | no | Project status filters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFields": [
        {}
      ],
      "lookup": "string",
      "name": "Ava Chen",
      "projects": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFields` | array<object> |  |
| `lookup` | string |  |
| `name` | string |  |
| `projects` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native DateX API, this operation is `POST owners/get` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-owners.md) for the provider-specific parameters and requirements.

