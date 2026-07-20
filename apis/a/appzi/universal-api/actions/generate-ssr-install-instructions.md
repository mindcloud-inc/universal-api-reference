# Appzi: Generate SSR Install Instructions

Generates SSR install snippets for Appzi.

```
POST https://connect.mindcloud.co/v1/universal/appzi/latest/actions/generate-ssr-install-instructions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appzi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appzi/latest/actions/generate-ssr-install-instructions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "portalToken": "string",
  "framework": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appzi/latest/actions/generate-ssr-install-instructions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "portalToken": "string",
    "framework": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `portalToken` | string | yes | Portal token inserted into the generated SSR install snippet. |
| `framework` | string | yes | SSR framework documented by Appzi: next-app-router, next-pages-router, nuxt, sveltekit, or jekyll. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Appzi API returns.

## Native endpoint

Through the native Appzi API, this operation is `GET https://docs.appzi.io/installation/` (base URL `https://api.appzi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-ssr-install-instructions.md) for the provider-specific parameters and requirements.

