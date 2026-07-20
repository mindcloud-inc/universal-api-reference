# Look Digital Signage: Trigger Action

Triggers a configured action in Look Digital Signage.

```
PUT https://connect.mindcloud.co/v1/universal/lookDigitalSignage/latest/actions/trigger-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Look Digital Signage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lookDigitalSignage/latest/actions/trigger-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionLink": "https://...your-look-action-link..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lookDigitalSignage/latest/actions/trigger-action', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actionLink": "https://...your-look-action-link..."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actionLink` | string | yes | Paste the full Action Link from Look Action settings. Example: `https://...your-look-action-link...`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Look Digital Signage API returns.

## Native endpoint

Through the native Look Digital Signage API, this operation is `GET https://api.lookit.hk/api/v1/external/actions/:actionLink` (base URL `https://api.lookit.hk/api/v1/external/actions`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-action.md) for the provider-specific parameters and requirements.

