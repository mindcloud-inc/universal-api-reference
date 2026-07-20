# Switchy.io: List Workspaces

Retrieves workspaces from Switchy.io.

```
GET https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Switchy.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/list-workspaces?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string |  |
| `createdDate` | date |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Switchy.io API, this operation is `POST /v1/graphql` (base URL `https://graphql.switchy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

