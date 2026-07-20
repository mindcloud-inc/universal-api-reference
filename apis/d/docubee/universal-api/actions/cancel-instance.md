# Docubee: Cancel Instance

Cancels or removes a Docubee workflow instance.

```
DELETE https://connect.mindcloud.co/v1/universal/docubee/latest/actions/cancel-instance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docubee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/cancel-instance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docubee/latest/actions/cancel-instance?${params}`, {
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
| `instanceId` | string | no | The workflow instance ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "instanceId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `instanceId` | string | The canceled workflow instance ID. |
| `status` | string | The workflow instance status after cancellation. |

## Native endpoint

Through the native Docubee API, this operation is `DELETE /instances/:instanceId` (base URL `https://docubee.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-instance.md) for the provider-specific parameters and requirements.

