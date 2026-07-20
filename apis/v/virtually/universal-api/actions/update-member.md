# Virtually: Update Member

Updates an existing member in Virtually.

```
PUT https://connect.mindcloud.co/v1/universal/virtually/latest/actions/update-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Virtually `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/update-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "memberId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/virtually/latest/actions/update-member', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "memberId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `memberId` | string | yes | The member ID. |
| `name` | string | no | The member name. |
| `email` | string | no | The member email address. |
| `tagIds[]` | array<string> | no | The tag IDs to assign to the member. |
| `properties` | object | no | Additional member properties. |
| `status` | string | no | The member status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Virtually API, this operation is `PATCH /api/v2/orgs/:orgId/members/:memberId` (base URL `https://app.tryvirtually.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-member.md) for the provider-specific parameters and requirements.

