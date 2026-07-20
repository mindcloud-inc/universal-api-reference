# Mixpanel: List Top Events

Retrieves top events from Mixpanel.

```
GET https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/list-top-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mixpanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/list-top-events?connectionId=$CONNECTION_ID&type=general" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "general"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/list-top-events?${params}`, {
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
| `type` | string | yes | Analysis type: general, unique, or average. Example: `general`. |
| `limit` | number | no | Maximum number of event names to return. Example: `50`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | no | Required when authenticating with a Mixpanel service account. Example: `12345`. |
| `workspaceId` | number | no | Optional Mixpanel workspace ID. Example: `98765`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mixpanel API returns.

## Native endpoint

Through the native Mixpanel API, this operation is `GET /query/events/names` (base URL `https://mixpanel.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-top-events.md) for the provider-specific parameters and requirements.

