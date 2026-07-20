# fal.ai: Delete Request Payloads

Deletes fal.ai request payloads and output files.

```
DELETE https://connect.mindcloud.co/v1/universal/falai/latest/actions/delete-request-payloads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fal.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/falai/latest/actions/delete-request-payloads?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/falai/latest/actions/delete-request-payloads?${params}`, {
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
| `requestId` | string | yes | fal.ai request ID whose payloads should be deleted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cdn_delete_results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cdn_delete_results` | array<object> |  |

## Native endpoint

Through the native fal.ai API, this operation is `DELETE /models/requests/:requestId/payloads` (base URL `https://api.fal.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-request-payloads.md) for the provider-specific parameters and requirements.

