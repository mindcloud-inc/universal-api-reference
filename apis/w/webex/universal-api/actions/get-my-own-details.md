# Webex: Get My Own Details

Retrieves your own profile details from Webex.

```
GET https://connect.mindcloud.co/v1/universal/webex/latest/actions/get-my-own-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webex/latest/actions/get-my-own-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webex/latest/actions/get-my-own-details?${params}`, {
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
      "avatar": "https://example.com",
      "created": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "emails": [
        "ava@example.com"
      ],
      "firstName": "Ava",
      "id": "string",
      "lastActivity": "2026-05-07T12:00:00.000Z",
      "lastModified": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "licenses": [
        "string"
      ],
      "nickName": "Ava Chen",
      "orgId": "string",
      "phoneNumbers": [
        {}
      ],
      "status": "string",
      "timezone": "string",
      "type": "string",
      "userName": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string | Avatar URL for the person. |
| `created` | date | Person creation timestamp. |
| `displayName` | string | Person display name. |
| `emails` | array<string> | Email addresses associated with the person. |
| `firstName` | string | Person first name. |
| `id` | string | Person identifier. |
| `lastActivity` | date | Most recent activity timestamp. |
| `lastModified` | date | Last modification timestamp. |
| `lastName` | string | Person last name. |
| `licenses` | array<string> | License identifiers assigned to the person. |
| `nickName` | string | Person nickname. |
| `orgId` | string | Organization identifier for the person. |
| `phoneNumbers` | array<object> | Phone numbers associated with the person. |
| `status` | string | Person status. |
| `timezone` | string | Person timezone. |
| `type` | string | Person account type. |
| `userName` | string | Username for the person. |

## Native endpoint

Through the native Webex API, this operation is `GET /people/me` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-own-details.md) for the provider-specific parameters and requirements.

