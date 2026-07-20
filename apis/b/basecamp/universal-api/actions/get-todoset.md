# Basecamp: Get Todoset

Retrieves a to-do set from Basecamp.

```
GET https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/get-todoset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Basecamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/get-todoset?connectionId=$CONNECTION_ID&accountId=6172410&todosetId=9660796830" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "6172410",
  "todosetId": "9660796830"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/get-todoset?${params}`, {
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
| `accountId` | string | yes | Basecamp account ID (numeric string). Example: `6172410`. |
| `todosetId` | number | yes | To-do set ID from the project's dock.todoset entry. Example: `9660796830`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Basecamp API returns.

## Native endpoint

Through the native Basecamp API, this operation is `GET /:accountId/todosets/:todosetId.json` (base URL `https://3.basecampapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-todoset.md) for the provider-specific parameters and requirements.

