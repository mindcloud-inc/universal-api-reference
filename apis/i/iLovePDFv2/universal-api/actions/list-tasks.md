# iLovePDFv2: List Tasks



```
GET https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDFv2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/list-tasks?${params}`, {
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
| `page` | number | no | Task results page. iLoveAPI returns 50 tasks per page. Default: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tool` | string | no | Optional tool filter. |
| `status` | string | no | Optional task status filter such as TaskSuccess. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native iLovePDFv2 API returns.

## Native endpoint

Through the native iLovePDFv2 API, this operation is `GET /task` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

