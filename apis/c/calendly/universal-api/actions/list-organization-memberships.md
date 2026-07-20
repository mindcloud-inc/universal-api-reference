# Calendly: List Organization Memberships

Retrieves organization memberships from Calendly.

```
GET https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-organization-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calendly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-organization-memberships?connectionId=$CONNECTION_ID&limit=25&offset=0&organization=https%3A%2F%2Fapi.calendly.com%2Forganizations%2Fe684df12-9454-43ef-8fc4-2d0faa4ec21e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organization": "https://api.calendly.com/organizations/e684df12-9454-43ef-8fc4-2d0faa4ec21e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-organization-memberships?${params}`, {
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
| `organization` | list | yes | Organization URI filter. One of: `https://api.calendly.com/organizations/e684df12-9454-43ef-8fc4-2d0faa4ec21e`. Default: `https://api.calendly.com/organizations/e684df12-9454-43ef-8fc4-2d0faa4ec21e`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collection": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collection` | array<object> | List of organization membership records. |
| `pagination` | object | Pagination metadata for list traversal. |

## Native endpoint

Through the native Calendly API, this operation is `GET /organization_memberships` (base URL `https://api.calendly.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organization-memberships.md) for the provider-specific parameters and requirements.

