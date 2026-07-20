# Quantcast: List Team Members

Retrieves team members from Quantcast.

```
GET https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-team-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-team-members?connectionId=$CONNECTION_ID&organizationId=88297" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "88297"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-team-members?${params}`, {
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
| `organizationId` | number | yes | Quantcast organization identifier required to list team members. Default: `88297`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "teamMembers": {
        "edges": {
          "teamId": 1,
          "userId": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `teamMembers` | object | Team members connection returned by Quantcast. |
| `teamMembers.edges` | array<object> | Team member nodes in the result set. |
| `teamMembers.edges.teamId` | number | Quantcast team identifier. |
| `teamMembers.edges.userId` | string | Quantcast user identifier. |

## Native endpoint

Through the native Quantcast API, this operation is `GET /api/v2/graphql` (base URL `https://developers.quantcast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-members.md) for the provider-specific parameters and requirements.

