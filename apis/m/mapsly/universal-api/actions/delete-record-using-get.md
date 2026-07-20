# Mapsly: Delete Record Using GET

Deletes a record from Mapsly using GET.

```
DELETE https://connect.mindcloud.co/v1/universal/mapsly/latest/actions/delete-record-using-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mapsly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mapsly/latest/actions/delete-record-using-get?connectionId=$CONNECTION_ID&entity=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entity": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mapsly/latest/actions/delete-record-using-get?${params}`, {
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
| `entity` | string | yes | The Mapsly entity API name to target, such as Leads. |
| `id` | string | yes | The record identifier to delete. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callbackUrl` | string | no | Optional URL to receive async processing results. |
| `passthrough` | string | no | Optional value echoed back in callback payloads. |
| `async` | boolean | no | Queue the request instead of processing it synchronously. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mapsly API returns.

## Native endpoint

Through the native Mapsly API, this operation is `GET /deleterecord` (base URL `https://api.mapsly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-record-using-get.md) for the provider-specific parameters and requirements.

