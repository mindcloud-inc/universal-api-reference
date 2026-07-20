# Ghost: List Members

Retrieves members from Ghost.

```
GET https://connect.mindcloud.co/v1/universal/ghost/latest/actions/list-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ghost `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ghost/latest/actions/list-members?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ghost/latest/actions/list-members?${params}`, {
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
| `include` | string | no | Comma-separated related resources to include, such as labels or newsletters. |

## Response

```json
{
  "success": true,
  "data": [
    {
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

Through the native Ghost API, this operation is `GET /members/` (base URL `{{credentials.adminDomain}}/ghost/api/admin`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-members.md) for the provider-specific parameters and requirements.

