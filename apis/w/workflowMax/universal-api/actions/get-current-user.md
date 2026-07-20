# WorkflowMax: Get Current User



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-current-user?${params}`, {
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
      "Organization": {
        "Name": "Ava Chen"
      },
      "User": {
        "Email": "ava@example.com",
        "Name": "Ava Chen",
        "UUID": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Organization.Name` | string | The name of the organization. |
| `User.Email` | string | The email of the organization user. |
| `User.Name` | string | The name of the organization user. |
| `User.UUID` | string | The unique identifier of the organization user. |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/me` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

