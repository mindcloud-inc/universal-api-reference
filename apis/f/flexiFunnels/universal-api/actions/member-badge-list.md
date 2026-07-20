# FlexiFunnels: Member Badge List

Retrieves member badges from FlexiFunnels.

```
GET https://connect.mindcloud.co/v1/universal/flexiFunnels/latest/actions/member-badge-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlexiFunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexiFunnels/latest/actions/member-badge-list?connectionId=$CONNECTION_ID&funnelPageId=1027516&courseId=91090&lessonId=545366" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "funnelPageId": "1027516",
  "courseId": "91090",
  "lessonId": "545366"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexiFunnels/latest/actions/member-badge-list?${params}`, {
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
| `funnelPageId` | number | yes | Default: `1027516`. |
| `courseId` | number | yes | Default: `91090`. |
| `lessonId` | number | yes | Default: `545366`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FlexiFunnels API returns.

## Native endpoint

Through the native FlexiFunnels API, this operation is `POST /api/member-badge-list` (base URL `https://bridge.flexifunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/member-badge-list.md) for the provider-specific parameters and requirements.

