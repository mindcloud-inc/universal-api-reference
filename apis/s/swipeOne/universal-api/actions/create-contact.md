# Swipe One: Create Contact



```
POST https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swipe One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address.city` | string | no |  |
| `address.country` | string | no |  |
| `address.line1` | string | no |  |
| `address.line2` | string | no |  |
| `address.state` | string | no |  |
| `address.zipcode` | string | no |  |
| `department` | string | no |  |
| `gender` | string | no |  |
| `industry` | string | no |  |
| `occupation` | string | no |  |
| `socialMediaUrls.facebook` | string | no |  |
| `socialMediaUrls.linkedin` | string | no |  |
| `socialMediaUrls.twitter` | string | no |  |
| `timezone` | string | no |  |
| `website` | string | no |  |
| `workspaceId` | string | yes |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `fullName` | string | no |  |
| `email` | string | no |  |
| `phone` | string | no |  |
| `address` | object | no |  |
| `birthday` | date | no |  |
| `socialMediaUrls` | object | no |  |
| `teamSize` | number | no |  |
| `annualRevenue` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "contact": {
          "_id": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "createdBy": {
            "id": "string",
            "name": "Ava Chen",
            "type": "string"
          },
          "email": "ava@example.com",
          "firstName": "Ava",
          "fullName": "Ava Chen",
          "lastName": "Chen",
          "tags": [
            "string"
          ],
          "workspaceId": "string"
        }
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.contact` | object |  |
| `data.contact._id` | string |  |
| `data.contact.createdAt` | date |  |
| `data.contact.createdBy` | object |  |
| `data.contact.createdBy.id` | string |  |
| `data.contact.createdBy.name` | string |  |
| `data.contact.createdBy.type` | string |  |
| `data.contact.email` | string |  |
| `data.contact.firstName` | string |  |
| `data.contact.fullName` | string |  |
| `data.contact.lastName` | string |  |
| `data.contact.tags` | array<string> |  |
| `data.contact.workspaceId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Swipe One API, this operation is `POST /workspaces/:workspaceId/contacts` (base URL `https://api.swipeone.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

