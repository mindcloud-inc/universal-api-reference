# InstantCard Universal API Examples

These examples use the MindCloud API key and InstantCard connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Profile

Retrieves the authenticated user profile from InstantCard.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-my-profile?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": 1,
      "organization": {
        "organizationId": 1,
        "organizationName": "Ava Chen"
      },
      "organizationId": 1,
      "organizationName": "Ava Chen",
      "settings": {
        "fullName": "Ava Chen",
        "notifications": {
          "orderConfirmation": true,
          "orderPrintedConfirmation": true
        },
        "pageSize": 1,
        "showPhoto": true
      }
    }
  ],
  "meta": {}
}
```

See the full [Get My Profile action reference](actions/get-my-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/instantCard/latest/actions/get-my-profile).

## Add Cards To Print Job

Updates an existing print job in InstantCard by adding cards.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/add-cards-to-print-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": 1,
  "id": 1,
  "cardIds": "3096409,3145927"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/add-cards-to-print-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": 1,
    "id": 1,
    "cardIds": "3096409,3145927"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "address_id": 1,
      "created_at": "string",
      "extract": {},
      "id": 1,
      "list_users": [
        {}
      ],
      "organization": {},
      "status": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Cards To Print Job action reference](actions/add-cards-to-print-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/instantCard/latest/actions/add-cards-to-print-job).
