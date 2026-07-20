# Currents: List Projects



```
GET https://connect.mindcloud.co/v1/universal/currents/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Currents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currents/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/currents/latest/actions/list-projects?${params}`, {
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
| `endingBefore` | string | no |  |
| `limit` | string | no |  |
| `startingAfter` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "createdAt": "string",
          "cursor": "string",
          "defaultBranchName": "Ava Chen",
          "failFast": true,
          "inactivityTimeoutSeconds": 1,
          "name": "Ava Chen",
          "projectId": "string"
        }
      ],
      "has_more": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].createdAt` | string |  |
| `data[].cursor` | string |  |
| `data[].defaultBranchName` | string |  |
| `data[].failFast` | boolean |  |
| `data[].inactivityTimeoutSeconds` | number |  |
| `data[].name` | string |  |
| `data[].projectId` | string |  |
| `has_more` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native Currents API, this operation is `GET /projects` (base URL `https://api.currents.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

