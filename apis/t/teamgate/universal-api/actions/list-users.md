# Teamgate: List Users

Retrieves users from Teamgate.

```
GET https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamgate `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-users?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accountUrl": "https://example.com",
      "created": {
        "time": "string"
      },
      "currencies": [
        {
          "fullRate": "string",
          "iso": "string",
          "name": "Ava Chen",
          "rate": "string",
          "symbol": "string"
        }
      ],
      "defaultCurrency": "string",
      "email": "ava@example.com",
      "id": 1,
      "isActive": "string",
      "language": {
        "code": "string",
        "name": "Ava Chen"
      },
      "lastLogin": {
        "time": "string"
      },
      "locale": "string",
      "name": "Ava Chen",
      "permissions": {
        "companies": [
          {}
        ],
        "deals": [
          {}
        ],
        "events": [
          {}
        ],
        "leads": [
          {}
        ],
        "people": [
          {}
        ],
        "settingsUsersGroups": [
          {}
        ]
      },
      "picture": {
        "large": "string",
        "medium": "string",
        "small": "string"
      },
      "role": "string",
      "surname": "Ava Chen",
      "timeZone": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountUrl` | string |  |
| `created.time` | string |  |
| `currencies[].fullRate` | string |  |
| `currencies[].iso` | string |  |
| `currencies[].name` | string |  |
| `currencies[].rate` | string |  |
| `currencies[].symbol` | string |  |
| `defaultCurrency` | string |  |
| `email` | string |  |
| `id` | number |  |
| `isActive` | string |  |
| `language.code` | string |  |
| `language.name` | string |  |
| `lastLogin.time` | string |  |
| `locale` | string |  |
| `name` | string |  |
| `permissions.companies[]` | object |  |
| `permissions.deals[]` | object |  |
| `permissions.events[]` | object |  |
| `permissions.leads[]` | object |  |
| `permissions.people[]` | object |  |
| `permissions.settingsUsersGroups[]` | object |  |
| `picture.large` | string |  |
| `picture.medium` | string |  |
| `picture.small` | string |  |
| `role` | string |  |
| `surname` | string |  |
| `timeZone` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Teamgate API, this operation is `GET /users` (base URL `https://api.teamgate.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

