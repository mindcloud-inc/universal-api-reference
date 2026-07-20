# Leverly: Stop Call



```
DELETE https://connect.mindcloud.co/v1/universal/leverly/latest/actions/stop-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leverly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/leverly/latest/actions/stop-call?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leverly/latest/actions/stop-call?${params}`, {
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
| `vendorLeadId` | string | no | Vendor lead ID from your system. It must have been included in the original post. |
| `phone1` | string | no | Lead phone number in 1NNNNNNNNNN format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "data": "string",
      "message": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Failure-path error code from Stop Call runtime evidence. |
| `data` | string | Failure-path provider response text from Stop Call runtime evidence. |
| `message` | string | Failure-path error message from Stop Call runtime evidence. |
| `name` | string | Failure-path error object field from Stop Call runtime evidence. |

## Native endpoint

Through the native Leverly API, this operation is `POST /inquiry/unpark` (base URL `https://app.leverly.com/main`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stop-call.md) for the provider-specific parameters and requirements.

