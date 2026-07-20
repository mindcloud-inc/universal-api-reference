# EmailListVerify: Download Email List

Downloads a finished email list from EmailListVerify.

```
GET https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/download-email-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailListVerify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/download-email-list?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/download-email-list?${params}`, {
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
| `id` | string | yes | Finished email list ID to download. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EmailListVerify API returns.

## Native endpoint

Through the native EmailListVerify API, this operation is `GET /api/maillists/:id` (base URL `https://api.emaillistverify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-email-list.md) for the provider-specific parameters and requirements.

