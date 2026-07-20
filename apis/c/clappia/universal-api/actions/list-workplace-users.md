# Clappia: List Workplace Users

Retrieves workplace users from your Clappia workplace.

```
GET https://connect.mindcloud.co/v1/universal/clappia/latest/actions/list-workplace-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clappia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/list-workplace-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clappia/latest/actions/list-workplace-users?${params}`, {
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
| `pageSize` | number | no | Maximum number of users to return. Default: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `token` | string | no | Token returned by a previous workplace users response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canCreateApps": "string",
      "emailAddress": "ava@example.com",
      "name": "Ava Chen",
      "phoneNumber": "string",
      "role": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canCreateApps` | string | Whether the user can create apps in the workplace. |
| `emailAddress` | string | Workplace user email address. |
| `name` | string | Workplace user display name. |
| `phoneNumber` | string | Workplace user phone number. |
| `role` | string | Workplace role for the user. |
| `status` | string | Current workplace user status. |

## Native endpoint

Through the native Clappia API, this operation is `POST /workplace/getWorkplaceUsers` (base URL `https://api-public-v4.clappia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workplace-users.md) for the provider-specific parameters and requirements.

