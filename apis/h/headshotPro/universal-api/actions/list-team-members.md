# HeadshotPro: List Team Members

Retrieves team members from HeadshotPro.

```
GET https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/list-team-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HeadshotPro `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/list-team-members?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/list-team-members?${params}`, {
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
| `status` | string | no | Optional member status filter: accepted, pending, or finished. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "members": [
        {}
      ],
      "pagination": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `members` | array<object> | Members returned by the query. |
| `pagination` | object | Pagination details for the result page. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native HeadshotPro API, this operation is `GET /organization/team` (base URL `https://server.headshotpro.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-team-members.md) for the provider-specific parameters and requirements.

