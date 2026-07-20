# Bannerbite: List Bites

Retrieves bites from a Bannerbite project.

```
GET https://connect.mindcloud.co/v1/universal/bannerbite/latest/actions/list-bites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bannerbite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bannerbite/latest/actions/list-bites?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bannerbite/latest/actions/list-bites?${params}`, {
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
| `limit` | number | no | Number of bites to return. Bannerbite defaults to 10 and supports up to 100. Default: `10`. |
| `projectId` | number | yes | The project ID whose bites you want to list. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bannerbite API returns.

## Native endpoint

Through the native Bannerbite API, this operation is `GET /api/bites` (base URL `https://api.bannerbite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bites.md) for the provider-specific parameters and requirements.

