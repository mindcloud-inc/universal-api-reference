# Quantcast: List Members

Retrieves organization members from Quantcast.

```
GET https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-members?connectionId=$CONNECTION_ID&organizationId=88297" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "88297"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-members?${params}`, {
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
| `organizationId` | number | yes | Quantcast organization identifier required to list members. Default: `88297`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "members": {
        "edges": {
          "userEmail": "ava@example.com",
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
| `members` | object | Members connection returned by Quantcast. |
| `members.edges` | array<object> | Member nodes in the result set. |
| `members.edges.userEmail` | string | Member email address. |
| `members.edges.userId` | string | Quantcast user identifier. |

## Native endpoint

Through the native Quantcast API, this operation is `GET /api/v2/graphql` (base URL `https://developers.quantcast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-members.md) for the provider-specific parameters and requirements.

