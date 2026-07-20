# ParseHub: Get Last Ready Data (JSON)



```
GET https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/get-last-ready-data-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ParseHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/get-last-ready-data-json?connectionId=$CONNECTION_ID&projectToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/get-last-ready-data-json?${params}`, {
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
| `projectToken` | string | yes | The ParseHub token of the project whose latest ready data you want. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ParseHub API returns.

## Native endpoint

Through the native ParseHub API, this operation is `GET /projects/{project_token}/last_ready_run/data` (base URL `https://www.parsehub.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-last-ready-data-json.md) for the provider-specific parameters and requirements.

