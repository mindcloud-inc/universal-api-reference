# Docubee: Delete Signature Process

Deletes a signature process from Docubee.

```
DELETE https://connect.mindcloud.co/v1/universal/docubee/latest/actions/delete-signature-process
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docubee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/delete-signature-process?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docubee/latest/actions/delete-signature-process?${params}`, {
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
| `processId` | string | no | The signature process ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "processId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `processId` | string | The deleted signature process ID. |
| `status` | string | The signature process status after deletion. |

## Native endpoint

Through the native Docubee API, this operation is `DELETE /signatures/:processId` (base URL `https://docubee.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-signature-process.md) for the provider-specific parameters and requirements.

