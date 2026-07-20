# Mixpanel: List Top Event Properties

Retrieves top event properties from Mixpanel.

```
GET https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/list-top-event-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mixpanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/list-top-event-properties?connectionId=$CONNECTION_ID&event=Signed%20Up" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "event": "Signed Up"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/list-top-event-properties?${params}`, {
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
| `event` | string | yes | Single event name to inspect. Example: `Signed Up`. |
| `limit` | number | no | Maximum number of properties to return. Example: `20`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | no | Required when authenticating with a Mixpanel service account. Example: `12345`. |
| `workspaceId` | number | no | Optional Mixpanel workspace ID. Example: `98765`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mixpanel API returns.

## Native endpoint

Through the native Mixpanel API, this operation is `GET /query/events/properties/top` (base URL `https://mixpanel.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-top-event-properties.md) for the provider-specific parameters and requirements.

