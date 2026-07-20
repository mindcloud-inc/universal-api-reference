# SonarQube: List User Groups For User

Retrieves user groups for a SonarQube user.

```
GET https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/list-user-groups-for-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SonarQube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/list-user-groups-for-user?connectionId=$CONNECTION_ID&login=string&organization=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "login": "string",
  "organization": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/list-user-groups-for-user?${params}`, {
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
| `login` | string | yes | User login. Required by /api/users/groups. |
| `organization` | string | yes | Organization key. Required by /api/users/groups. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groups": [
        {}
      ],
      "paging": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groups` | array<object> |  |
| `paging` | object |  |

## Native endpoint

Through the native SonarQube API, this operation is `GET /api/users/groups` (base URL `https://sonarcloud.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-groups-for-user.md) for the provider-specific parameters and requirements.

