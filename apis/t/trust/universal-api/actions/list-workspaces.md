# Trust: List Workspaces

Retrieves workspaces from Trust.

```
GET https://connect.mindcloud.co/v1/universal/trust/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trust `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trust/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trust/latest/actions/list-workspaces?${params}`, {
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
      "registeredWorkspaces": [
        "string"
      ],
      "workspaceDetails": [
        {
          "name": "Ava Chen",
          "website": "string",
          "workspaceId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `registeredWorkspaces` | array<string> |  |
| `workspaceDetails` | array<object> |  |
| `workspaceDetails[].name` | string |  |
| `workspaceDetails[].website` | string |  |
| `workspaceDetails[].workspaceId` | string |  |

## Native endpoint

Through the native Trust API, this operation is `GET /workspaces` (base URL `https://api.usetrust.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

