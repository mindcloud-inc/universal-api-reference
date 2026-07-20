# Availity: Delete Claim Status Inquiry

Deletes a claim status inquiry from Availity.

```
DELETE https://connect.mindcloud.co/v1/universal/availity/latest/actions/delete-claim-status-inquiry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Availity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/availity/latest/actions/delete-claim-status-inquiry?connectionId=$CONNECTION_ID&id=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/availity/latest/actions/delete-claim-status-inquiry?${params}`, {
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
| `id` | string | yes | Unique response ID for the claim status inquiry to delete. Example: `123`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Availity API returns.

## Native endpoint

Through the native Availity API, this operation is `DELETE /availity/v1/claim-statuses/{id}` (base URL `https://api.availity.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-claim-status-inquiry.md) for the provider-specific parameters and requirements.

