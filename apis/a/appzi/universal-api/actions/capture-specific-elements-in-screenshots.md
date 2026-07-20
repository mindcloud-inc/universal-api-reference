# Appzi: Capture Specific Elements In Screenshots

Retrieves a screenshot element-capture snippet from Appzi.

```
GET https://connect.mindcloud.co/v1/universal/appzi/latest/actions/capture-specific-elements-in-screenshots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appzi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appzi/latest/actions/capture-specific-elements-in-screenshots?connectionId=$CONNECTION_ID&portalToken=fYbQ6" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalToken": "fYbQ6"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appzi/latest/actions/capture-specific-elements-in-screenshots?${params}`, {
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
| `portalToken` | string | yes | Portal token used only to validate runtime against the existing Appzi probe surface and enrich the snippet output with current survey context. Example: `fYbQ6`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Appzi API returns.

## Native endpoint

Through the native Appzi API, this operation is `GET /api/probe/:portalToken` (base URL `https://api.appzi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/capture-specific-elements-in-screenshots.md) for the provider-specific parameters and requirements.

