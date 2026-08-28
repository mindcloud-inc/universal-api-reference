# MindCloud: Get Universal Action



```
GET https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/get-universal-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MindCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/get-universal-action?connectionId=$CONNECTION_ID&actionSlug=string&appSlug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actionSlug": "string",
  "appSlug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/get-universal-action?${params}`, {
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
| `actionSlug` | string | yes | Action Slug for this MindCloud v2 request. |
| `appSlug` | string | yes | App Slug for this MindCloud v2 request. |
| `fields` | string | no | Optional Fields query parameter documented by the MindCloud v2 API. |
| `version` | string | no | Optional Version query parameter documented by the MindCloud v2 API. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MindCloud API returns.

## Native endpoint

Through the native MindCloud API, this operation is `GET /v2/universal/apps/:appSlug/actions/:actionSlug` (base URL `https://connect.mindcloud.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-universal-action.md) for the provider-specific parameters and requirements.

