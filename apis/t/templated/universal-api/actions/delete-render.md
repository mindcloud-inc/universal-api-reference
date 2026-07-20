# Templated: Delete Render

Deletes an existing render from Templated.

```
DELETE https://connect.mindcloud.co/v1/universal/templated/latest/actions/delete-render
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Templated `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/templated/latest/actions/delete-render?connectionId=$CONNECTION_ID&renderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "renderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/templated/latest/actions/delete-render?${params}`, {
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
| `renderId` | string | yes | The render id of the render that will be deleted. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Templated API returns.

## Native endpoint

Through the native Templated API, this operation is `DELETE /v1/render/:id` (base URL `https://api.templated.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-render.md) for the provider-specific parameters and requirements.

