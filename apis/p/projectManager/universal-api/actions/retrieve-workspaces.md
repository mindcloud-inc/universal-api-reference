# ProjectManager: Retrieve Workspaces

Retrieves workspaces from ProjectManager.

```
GET https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-workspaces?${params}`, {
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
      "businessUserId": "string",
      "color": "string",
      "company": "string",
      "customerId": "string",
      "customProductDomain": "string",
      "id": "string",
      "isInviteAccepted": true,
      "isOwner": true,
      "isPaid": true,
      "organizationId": "string",
      "registerDate": "string",
      "roleName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessUserId` | string |  |
| `color` | string |  |
| `company` | string |  |
| `customerId` | string |  |
| `customProductDomain` | string |  |
| `id` | string |  |
| `isInviteAccepted` | boolean |  |
| `isOwner` | boolean |  |
| `isPaid` | boolean |  |
| `organizationId` | string |  |
| `registerDate` | string |  |
| `roleName` | string |  |

## Native endpoint

Through the native ProjectManager API, this operation is `GET /api/data/workspaces` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-workspaces.md) for the provider-specific parameters and requirements.

