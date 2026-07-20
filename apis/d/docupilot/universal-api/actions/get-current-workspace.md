# Docupilot: Get Current Workspace

Retrieves current workspace details from Docupilot.

```
GET https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/get-current-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docupilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/get-current-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/get-current-workspace?${params}`, {
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
      "active": true,
      "createdTime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "mfaEnforced": true,
      "orgName": "Ava Chen",
      "planId": "string",
      "planStatus": "string",
      "role": "string",
      "timezone": "string",
      "uniqueKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `createdTime` | date |  |
| `id` | number |  |
| `mfaEnforced` | boolean |  |
| `orgName` | string |  |
| `planId` | string |  |
| `planStatus` | string |  |
| `role` | string |  |
| `timezone` | string |  |
| `uniqueKey` | string |  |

## Native endpoint

Through the native Docupilot API, this operation is `GET /dashboard/accounts/v2/workspaces/current/` (base URL `https://api.docupilot.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-workspace.md) for the provider-specific parameters and requirements.

