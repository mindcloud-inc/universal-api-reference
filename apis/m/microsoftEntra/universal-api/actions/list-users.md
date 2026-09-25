# Microsoft Entra: List Users



```
GET https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Entra `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/list-users?${params}`, {
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
| `filter` | string | no | OData filter expression. Advanced queries require Include Count. Example: `startsWith(displayName,'A')`. |
| `search` | string | no | Search expression, such as "displayName:Ava". Requires Include Count. Example: `"displayName:Ava"`. |
| `count` | boolean | no | Include the matching count. Required for advanced search, filtering, and sorting. Example: `true`. |
| `select` | string | no | Comma-separated properties, such as id,displayName. Example: `id,displayName`. |
| `expand` | string | no | Related resources to include. Advanced directory queries do not support expand. Example: `manager`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "givenName": "Ava",
      "id": "string",
      "jobTitle": "string",
      "mail": "ava@example.com",
      "mobilePhone": "string",
      "officeLocation": "string",
      "preferredLanguage": "string",
      "surname": "Chen",
      "userPrincipalName": "ava@example.com"
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
| `mobilePhone` | string |  |
| `officeLocation` | string |  |
| `preferredLanguage` | string |  |
| `surname` | string |  |
| `userPrincipalName` | string |  |

## Native endpoint

Through the native Microsoft Entra API, this operation is `GET /users` (base URL `https://graph.microsoft.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

