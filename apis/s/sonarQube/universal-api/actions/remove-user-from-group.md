# SonarQube: Remove User From Group

Removes a user from a SonarQube user group.

```
DELETE https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/remove-user-from-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SonarQube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/remove-user-from-group?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/remove-user-from-group?${params}`, {
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
      "response": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | object | SonarQube Web API response payload. |
| `success` | boolean | Whether the operation completed successfully. |

## Native endpoint

Through the native SonarQube API, this operation is `POST /api/user_groups/remove_user` (base URL `https://sonarcloud.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-user-from-group.md) for the provider-specific parameters and requirements.

