# ActiveCampaign: Sync Contact

Finds a contact in ActiveCampaign, or creates one if no match is found.

```
POST https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/sync-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveCampaign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/sync-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact.email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/sync-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact.email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact` | object | no |  |
| `contact.email` | string | yes |  |
| `contact.firstName` | string | no |  |
| `contact.lastName` | string | no |  |
| `contact.phone` | string | no |  |
| `contact.fieldValues[]` | array<object> | no |  |
| `contact.deleted` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActiveCampaign API returns.

## Native endpoint

Through the native ActiveCampaign API, this operation is `POST /contact/sync` (base URL `{{credentials.apiUrl}}/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sync-contact.md) for the provider-specific parameters and requirements.

