# Astra: List Organization Users

Retrieves organization users from Astra.

```
GET https://connect.mindcloud.co/v1/universal/astra/latest/actions/list-organization-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Astra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/astra/latest/actions/list-organization-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/astra/latest/actions/list-organization-users?${params}`, {
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
      "OrgID": "string",
      "OrgName": "Ava Chen",
      "Users": [
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
| `OrgID` | string | The Astra organization ID. |
| `OrgName` | string | The Astra organization name. |
| `Users` | array<object> | The users in the organization. |

## Native endpoint

Through the native Astra API, this operation is `GET /v2/organizations/users` (base URL `https://api.astra.datastax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-users.md) for the provider-specific parameters and requirements.

