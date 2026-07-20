# Linear: Query

Makes an authenticated raw GraphQL request to Linear.

```
GET https://connect.mindcloud.co/v1/universal/linear/latest/actions/query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linear/latest/actions/query?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linear/latest/actions/query?${params}`, {
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
| `query` | string | no |  |
| `variables` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "lead": "string",
      "name": "Ava Chen",
      "startDate": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "targetDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `lead` | string |  |
| `name` | string |  |
| `startDate` | date |  |
| `state` | string |  |
| `targetDate` | date |  |

## Native endpoint

Through the native Linear API, this operation is `POST` (base URL `https://api.linear.app/graphql/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query.md) for the provider-specific parameters and requirements.

