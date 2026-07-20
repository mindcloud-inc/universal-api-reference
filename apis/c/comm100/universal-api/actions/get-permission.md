# Comm100: Get Permission

Retrieves a permission from Comm100 settings.

```
GET https://connect.mindcloud.co/v1/universal/comm100/latest/actions/get-permission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Comm100 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comm100/latest/actions/get-permission?connectionId=$CONNECTION_ID&permissionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "permissionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/comm100/latest/actions/get-permission?${params}`, {
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
| `permissionId` | number | yes | The Comm100 permission ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Comm100 API returns.

## Native endpoint

Through the native Comm100 API, this operation is `GET global/permissions/{{id}}` (base URL `https://api17.comm100.io/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-permission.md) for the provider-specific parameters and requirements.

