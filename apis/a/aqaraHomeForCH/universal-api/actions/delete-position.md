# Aqara Home for CH: Delete Position

Deletes an existing position from Aqara Home for CH.

```
DELETE https://connect.mindcloud.co/v1/universal/aqaraHomeForCH/latest/actions/delete-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aqara Home for CH `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/aqaraHomeForCH/latest/actions/delete-position?connectionId=$CONNECTION_ID&data=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aqaraHomeForCH/latest/actions/delete-position?${params}`, {
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
| `data` | object | yes | Aqara request data object for the selected intent. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aqara Home for CH API returns.

## Native endpoint

Through the native Aqara Home for CH API, this operation is `POST /v3.0/open/api` (base URL `https://open-cn.aqara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-position.md) for the provider-specific parameters and requirements.

