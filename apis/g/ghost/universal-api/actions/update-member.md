# Ghost: Update Member

Updates an existing member in Ghost.

```
PUT https://connect.mindcloud.co/v1/universal/ghost/latest/actions/update-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ghost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ghost/latest/actions/update-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ghost/latest/actions/update-member', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Ghost member ID from the URL path. |
| `members[0].email` | string | no | Email address for the member. |
| `members[0].name` | string | no | Updated display name for the member. |
| `members[0].labels[]` | array<string> | no | Updated member labels. Example: `label-a,label-b`. |
| `members[0].newsletters[]` | array<string> | no | Updated newsletters for the member. Example: `newsletter-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attribution": {
        "id": {},
        "referrerMedium": "string",
        "referrerSource": "string",
        "referrerUrl": {},
        "title": {},
        "type": {},
        "url": {}
      },
      "avatarImage": "string",
      "canComment": true,
      "commenting": {
        "disabled": true,
        "disabledReason": {},
        "disabledUntil": {}
      },
      "comped": true,
      "createdAt": "string",
      "email": "ava@example.com",
      "emailCount": 1,
      "emailOpenedCount": 1,
      "emailOpenRate": {},
      "emailSuppression": {
        "info": {},
        "suppressed": true
      },
      "geolocation": {},
      "id": "string",
      "lastSeenAt": {},
      "name": "Ava Chen",
      "newsletters": [
        {
          "description": {},
          "id": "string",
          "name": "Ava Chen",
          "status": "string"
        }
      ],
      "note": {},
      "status": "string",
      "subscribed": true,
      "unsubscribeUrl": "https://example.com",
      "updatedAt": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attribution.id` | object |  |
| `attribution.referrerMedium` | string |  |
| `attribution.referrerSource` | string |  |
| `attribution.referrerUrl` | object |  |
| `attribution.title` | object |  |
| `attribution.type` | object |  |
| `attribution.url` | object |  |
| `avatarImage` | string |  |
| `canComment` | boolean |  |
| `commenting.disabled` | boolean |  |
| `commenting.disabledReason` | object |  |
| `commenting.disabledUntil` | object |  |
| `comped` | boolean |  |
| `createdAt` | string |  |
| `email` | string |  |
| `emailCount` | number |  |
| `emailOpenedCount` | number |  |
| `emailOpenRate` | object |  |
| `emailSuppression.info` | object |  |
| `emailSuppression.suppressed` | boolean |  |
| `geolocation` | object |  |
| `id` | string |  |
| `lastSeenAt` | object |  |
| `name` | string |  |
| `newsletters[].description` | object |  |
| `newsletters[].id` | string |  |
| `newsletters[].name` | string |  |
| `newsletters[].status` | string |  |
| `note` | object |  |
| `status` | string |  |
| `subscribed` | boolean |  |
| `unsubscribeUrl` | string |  |
| `updatedAt` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Ghost API, this operation is `PUT /members/:id/` (base URL `{{credentials.adminDomain}}/ghost/api/admin`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-member.md) for the provider-specific parameters and requirements.

