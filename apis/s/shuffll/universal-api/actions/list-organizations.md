# Shuffll: List Organizations

Retrieves organizations from Shuffll.

```
GET https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/list-organizations?${params}`, {
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
      "branding": {},
      "id": "string",
      "isAllowedToUseOrganization": true,
      "isDefaultForUser": true,
      "name": "Ava Chen",
      "userCount": 1,
      "workspaces": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branding` | object | Branding settings for the organization. |
| `id` | string | Organization identifier. |
| `isAllowedToUseOrganization` | boolean | Whether the user can use the organization. |
| `isDefaultForUser` | boolean | Whether this organization is the default for the user. |
| `name` | string | Organization name. |
| `userCount` | number | Number of users in the organization. |
| `workspaces` | array<object> | Workspaces available in the organization. |

## Native endpoint

Through the native Shuffll API, this operation is `GET /auth/organization/list` (base URL `https://api.shuffll.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

