# SureCart: Retrieve Refund



```
GET https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-refund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-refund?connectionId=$CONNECTION_ID&id=7df72bb5-d1c1-43fb-bbd0-81651c1f53b2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "7df72bb5-d1c1-43fb-bbd0-81651c1f53b2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-refund?${params}`, {
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
| `id` | string | yes | The refund ID to retrieve. Example: `7df72bb5-d1c1-43fb-bbd0-81651c1f53b2`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SureCart API returns.

## Native endpoint

Through the native SureCart API, this operation is `GET v1/refunds/:id` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-refund.md) for the provider-specific parameters and requirements.

