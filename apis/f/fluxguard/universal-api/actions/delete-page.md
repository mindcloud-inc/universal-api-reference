# Fluxguard: Delete Page

Deletes a monitored page from Fluxguard.

```
DELETE https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/delete-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluxguard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/delete-page?connectionId=$CONNECTION_ID&siteId=string&sessionId=string&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "string",
  "sessionId": "string",
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/delete-page?${params}`, {
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
| `siteId` | string | yes |  |
| `sessionId` | string | yes |  |
| `pageId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fluxguard API returns.

## Native endpoint

Through the native Fluxguard API, this operation is `DELETE /site/:siteId/session/:sessionId/page/:pageId` (base URL `https://api.fluxguard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-page.md) for the provider-specific parameters and requirements.

