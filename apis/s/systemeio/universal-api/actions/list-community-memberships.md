# Systeme.io: List Community Memberships

Retrieves the collection of community memberships from Systeme.io.

```
GET https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/list-community-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Systeme.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/list-community-memberships?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/list-community-memberships?${params}`, {
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
| `community` | number | no | Community ID filter |
| `contact` | number | no | Contact ID filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "items": [
        {
          "community": {
            "domainName": "Ava Chen",
            "id": 1,
            "name": "Ava Chen",
            "path": "string"
          },
          "contact": {
            "id": 1
          },
          "id": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMore` | boolean | Whether more pages are available. |
| `items` | array<object> | List of memberships. |
| `items[].community.domainName` | string | Community domain name. |
| `items[].community.id` | number | Community ID. |
| `items[].community.name` | string | Community name. |
| `items[].community.path` | string | Community path. |
| `items[].contact.id` | number | Contact ID. |
| `items[].id` | number | Membership ID. |

## Native endpoint

Through the native Systeme.io API, this operation is `GET /api/community/memberships` (base URL `https://api.systeme.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-community-memberships.md) for the provider-specific parameters and requirements.

