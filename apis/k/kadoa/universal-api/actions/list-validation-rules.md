# Kadoa: List Validation Rules



```
GET https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/list-validation-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kadoa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/list-validation-rules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/list-validation-rules?${params}`, {
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
| `page` | number | no | Page number Default: `1`. |
| `pageSize` | number | no | Results per page Default: `50`. |
| `status` | string | no | Status: preview, enabled, disabled |
| `workflowId` | string | no | Filter by workflow ID |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kadoa API returns.

## Native endpoint

Through the native Kadoa API, this operation is `GET /v4/data-validation/rules` (base URL `https://api.kadoa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-validation-rules.md) for the provider-specific parameters and requirements.

