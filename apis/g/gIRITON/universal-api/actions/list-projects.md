# GIRITON: List Projects

Retrieves projects active on a selected GIRITON date.

```
GET https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GIRITON `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-projects?${params}`, {
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
| `dayFrom` | string | no | Starting date for included projects. |
| `departmentIds` | string | no | Comma-separated department IDs. |
| `dayTo` | string | no | End date for included projects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "entries": [
        {}
      ],
      "newestTimestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of returned entries. |
| `entries` | array<object> | Project entries. |
| `newestTimestamp` | date | Newest entry timestamp. |

## Native endpoint

Through the native GIRITON API, this operation is `GET /projects/projects` (base URL `https://rest.giriton.com/system/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

