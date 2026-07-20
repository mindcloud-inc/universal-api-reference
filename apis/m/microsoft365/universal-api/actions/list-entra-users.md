# Microsoft 365: List Entra Users

Retrieves Entra users from Microsoft 365.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-entra-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-entra-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-entra-users?${params}`, {
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
| `filter` | string | no | OData filter |
| `select` | string | no | OData select |
| `expand` | string | no | OData expand |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "givenName": "Ava Chen",
      "id": "string",
      "jobTitle": "string",
      "mail": "string",
      "mobilePhone": {},
      "officeLocation": "string",
      "preferredLanguage": "string",
      "surname": "Ava Chen",
      "userPrincipalName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `givenName` | string |  |
| `id` | string |  |
| `jobTitle` | string |  |
| `mail` | string |  |
| `mobilePhone` | object |  |
| `officeLocation` | string |  |
| `preferredLanguage` | string |  |
| `surname` | string |  |
| `userPrincipalName` | string |  |

## Native endpoint

Through the native Microsoft 365 API, this operation is `GET /v1.0/users` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-entra-users.md) for the provider-specific parameters and requirements.

