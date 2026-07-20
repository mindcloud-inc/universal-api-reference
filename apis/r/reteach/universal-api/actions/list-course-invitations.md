# Reteach: List Course Invitations



```
GET https://connect.mindcloud.co/v1/universal/reteach/latest/actions/list-course-invitations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reteach `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reteach/latest/actions/list-course-invitations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reteach/latest/actions/list-course-invitations?${params}`, {
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
| `customerIdentifier` | string | no | Filter by the customer id, email, username, or externalId. |
| `courseId` | string | no | Filter by the id of the course. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resultCount": 1,
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resultCount` | number | The total number of matching course invitations. |
| `results` | array<object> | The current page of course invitations. |

## Native endpoint

Through the native Reteach API, this operation is `GET /v1/course-invitation` (base URL `https://api.reteach.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-course-invitations.md) for the provider-specific parameters and requirements.

