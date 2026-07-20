# Dubsado: List Forms (Session Required)



```
GET https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/list-forms-session-required
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dubsado `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/list-forms-session-required?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/list-forms-session-required?${params}`, {
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
| `job` | string | no | Optional project ID filter observed in the Dubsado app bundle for /form reads. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dubsado API returns.

## Native endpoint

Through the native Dubsado API, this operation is `GET /form` (base URL `https://app.dubsado.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-forms-session-required.md) for the provider-specific parameters and requirements.

