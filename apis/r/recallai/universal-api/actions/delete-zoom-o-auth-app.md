# Recallai: Delete Zoom OAuth App

Deletes an existing Zoom OAuth app from Recallai.

```
DELETE https://connect.mindcloud.co/v1/universal/recallai/latest/actions/delete-zoom-o-auth-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/delete-zoom-o-auth-app?connectionId=$CONNECTION_ID&zoomOauthAppId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "zoomOauthAppId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recallai/latest/actions/delete-zoom-o-auth-app?${params}`, {
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
| `zoomOauthAppId` | string | yes | A UUID string identifying this zoom o auth app. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Recallai API returns.

## Native endpoint

Through the native Recallai API, this operation is `DELETE /api/v2/zoom-oauth-apps/:id/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-zoom-o-auth-app.md) for the provider-specific parameters and requirements.

