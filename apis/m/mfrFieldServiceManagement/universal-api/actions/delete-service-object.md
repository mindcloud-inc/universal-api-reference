# mfr Field Service Management: Delete Service Object

Deletes a service object from mfr Field Service Management.

```
DELETE https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/delete-service-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mfr Field Service Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/delete-service-object?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/delete-service-object?${params}`, {
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
| `id` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native mfr Field Service Management API returns.

## Native endpoint

Through the native mfr Field Service Management API, this operation is `DELETE ServiceObjects({{id}}L)` (base URL `https://portal.mobilefieldreport.com/odata`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-service-object.md) for the provider-specific parameters and requirements.

