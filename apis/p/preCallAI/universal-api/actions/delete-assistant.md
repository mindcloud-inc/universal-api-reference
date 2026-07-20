# PreCallAI: Delete Assistant

Deletes an existing assistant from PreCallAI.

```
DELETE https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/delete-assistant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PreCallAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/delete-assistant?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/delete-assistant?${params}`, {
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
| `id` | string | no | The assistant ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "status": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Optional provider payload returned for assistant deletion. |
| `message` | string | Provider status message for assistant deletion. |
| `status` | number | HTTP-style status returned by PreCallAI. |
| `success` | boolean | Whether the assistant delete request succeeded. |

## Native endpoint

Through the native PreCallAI API, this operation is `DELETE /user/deleteassistant` (base URL `https://api.precallai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-assistant.md) for the provider-specific parameters and requirements.

