# Week Plan: Get Workspaces



```
GET https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-workspaces?${params}`, {
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
      "Description": "string",
      "IsArchived": true,
      "Name": "Ava Chen",
      "StartOfWeek": 1,
      "UserCanAdministrate": true,
      "WorkspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Description` | string |  |
| `IsArchived` | boolean |  |
| `Name` | string |  |
| `StartOfWeek` | number |  |
| `UserCanAdministrate` | boolean |  |
| `WorkspaceId` | number |  |

## Native endpoint

Through the native Week Plan API, this operation is `GET workspaces` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspaces.md) for the provider-specific parameters and requirements.

