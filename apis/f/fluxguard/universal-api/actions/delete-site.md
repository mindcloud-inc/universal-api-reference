# Fluxguard: Delete Site

Deletes a site and its monitoring data from Fluxguard.

```
DELETE https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/delete-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluxguard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/delete-site?connectionId=$CONNECTION_ID&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/delete-site?${params}`, {
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

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fluxguard API returns.

## Native endpoint

Through the native Fluxguard API, this operation is `DELETE /site/:siteId` (base URL `https://api.fluxguard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-site.md) for the provider-specific parameters and requirements.

