# Unbounce: Delete Page Lead

Deletes a specific lead from an Unbounce page.

```
DELETE https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/delete-page-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unbounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/delete-page-lead?connectionId=$CONNECTION_ID&lead_id=string&page_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lead_id": "string",
  "page_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/delete-page-lead?${params}`, {
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
| `lead_id` | string | yes | Unbounce lead ID. |
| `page_id` | string | yes | Unbounce page ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Unbounce API returns.

## Native endpoint

Through the native Unbounce API, this operation is `DELETE /pages/:page_id/leads/:lead_id` (base URL `https://api.unbounce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-page-lead.md) for the provider-specific parameters and requirements.

