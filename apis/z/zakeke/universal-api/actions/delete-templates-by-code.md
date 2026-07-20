# Zakeke: Delete Templates By Code



```
DELETE https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/delete-templates-by-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zakeke `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/delete-templates-by-code?connectionId=$CONNECTION_ID&templateCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/delete-templates-by-code?${params}`, {
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
| `templateCode` | string | yes | Template code to delete across products. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zakeke API returns.

## Native endpoint

Through the native Zakeke API, this operation is `POST /v1/designs/templates/code/:templateCode/delete` (base URL `https://api.zakeke.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-templates-by-code.md) for the provider-specific parameters and requirements.

