# Pinghome: Update Statuspage

Updates an existing statuspage in Pinghome.

```
PUT https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-statuspage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-statuspage" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "statuspageId": "74f926a6-8cfc-4f11-86e6-46e7193813a8",
  "name": "MindCloud Status Updated",
  "description": "MindCloud public status page updated",
  "subdomain": "mc1749status",
  "type": "public"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-statuspage', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "statuspageId": "74f926a6-8cfc-4f11-86e6-46e7193813a8",
    "name": "MindCloud Status Updated",
    "description": "MindCloud public status page updated",
    "subdomain": "mc1749status",
    "type": "public"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `statuspageId` | string | yes | Statuspage ID to update. Example: `74f926a6-8cfc-4f11-86e6-46e7193813a8`. |
| `name` | string | yes | Updated statuspage name. Example: `MindCloud Status Updated`. |
| `description` | string | yes | Updated statuspage description. Example: `MindCloud public status page updated`. |
| `subdomain` | string | yes | Updated subdomain. Example: `mc1749status`. |
| `type` | string | yes | Updated statuspage type. Example: `public`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptionEnabled` | boolean | no | Whether public statuspage subscriptions are enabled. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `PUT /statuspage-cmd/v1/statuspage/:id` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-statuspage.md) for the provider-specific parameters and requirements.

