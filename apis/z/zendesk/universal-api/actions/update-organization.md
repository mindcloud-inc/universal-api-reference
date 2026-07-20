# Zendesk: Update Organization

Updates an existing organization in Zendesk.

```
PUT https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/update-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/update-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "46843791853460"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/update-organization', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "46843791853460"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Zendesk organization ID. Example: `46843791853460`. |
| `organization.name` | string | no | Updated organization name. Example: `Updated Organization Name`. |
| `organization.details` | string | no | Updated organization details. Example: `Updated organization details`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "details": "string",
      "domainNames": [
        "Ava Chen"
      ],
      "groupId": 1,
      "id": 1,
      "name": "Ava Chen",
      "sharedComments": true,
      "sharedTickets": true,
      "tags": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `details` | string |  |
| `domainNames[]` | string |  |
| `groupId` | number |  |
| `id` | number |  |
| `name` | string |  |
| `sharedComments` | boolean |  |
| `sharedTickets` | boolean |  |
| `tags[]` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Zendesk API, this operation is `PUT /organizations/:id.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-organization.md) for the provider-specific parameters and requirements.

