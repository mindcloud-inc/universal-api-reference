# Botsonic: Delete FAQ

Deletes an existing FAQ from Botsonic.

```
DELETE https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/delete-faq
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botsonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/delete-faq?connectionId=$CONNECTION_ID&faqId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "faqId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/delete-faq?${params}`, {
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
| `faqId` | string | yes | FAQ identifier to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Botsonic API returns.

## Native endpoint

Through the native Botsonic API, this operation is `DELETE /v1/business/bot-faq/:faqId` (base URL `https://api.botsonic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-faq.md) for the provider-specific parameters and requirements.

