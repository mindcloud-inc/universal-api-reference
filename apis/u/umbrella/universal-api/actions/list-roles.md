# Umbrella: List Roles

Retrieves user role definitions from Umbrella.

```
GET https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/list-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbrella `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/list-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/list-roles?${params}`, {
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
      "label": "string",
      "organizationId": 1,
      "roleId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `label` | string |  |
| `organizationId` | number |  |
| `roleId` | number |  |

## Native endpoint

Through the native Umbrella API, this operation is `GET /admin/v2/roles` (base URL `https://api.umbrella.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-roles.md) for the provider-specific parameters and requirements.

