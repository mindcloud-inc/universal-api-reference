# ActiveCampaign: Update Contact List Status

Updates a contact's list status in ActiveCampaign.

```
PUT https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/update-contact-list-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveCampaign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/update-contact-list-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactList.list": "string",
  "contactList.contact": "string",
  "contactList.status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/update-contact-list-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactList.list": "string",
    "contactList.contact": "string",
    "contactList.status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactList` | object | no |  |
| `contactList.list` | string | yes |  |
| `contactList.contact` | string | yes |  |
| `contactList.status` | string | yes |  |
| `contactList.sourceid` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActiveCampaign API returns.

## Native endpoint

Through the native ActiveCampaign API, this operation is `POST /contactLists` (base URL `{{credentials.apiUrl}}/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-list-status.md) for the provider-specific parameters and requirements.

