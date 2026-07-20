# Quantcast: List User Account Assignments

Retrieves user account assignments from Quantcast.

```
GET https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-user-account-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-user-account-assignments?connectionId=$CONNECTION_ID&organizationId=88297" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "88297"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-user-account-assignments?${params}`, {
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
| `organizationId` | number | yes | Quantcast organization identifier required to list user account assignments. Default: `88297`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "userAccountAssignments": {
        "edges": {
          "accountId": 1,
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
| `userAccountAssignments` | object | User account assignments connection returned by Quantcast. |
| `userAccountAssignments.edges` | array<object> | User account assignment nodes in the result set. |
| `userAccountAssignments.edges.accountId` | number | Quantcast account identifier assigned to the user. |
| `userAccountAssignments.edges.userId` | string | Quantcast user identifier. |

## Native endpoint

Through the native Quantcast API, this operation is `GET /api/v2/graphql` (base URL `https://developers.quantcast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-account-assignments.md) for the provider-specific parameters and requirements.

