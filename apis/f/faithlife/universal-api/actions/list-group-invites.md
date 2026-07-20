# Faithlife: List Group Invites

Retrieves a group's invites from Faithlife.

```
GET https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/list-group-invites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Faithlife `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/list-group-invites?connectionId=$CONNECTION_ID&limit=25&offset=0&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/list-group-invites?${params}`, {
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
| `groupId` | string | yes | The Faithlife group ID or token whose invites you want to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invites": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invites` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native Faithlife API, this operation is `GET /groups/:groupId/invites` (base URL `https://accountsapi.logos.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-group-invites.md) for the provider-specific parameters and requirements.

