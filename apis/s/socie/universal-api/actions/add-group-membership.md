# Socie: Add Group Membership



```
POST https://connect.mindcloud.co/v1/universal/socie/latest/actions/add-group-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/socie/latest/actions/add-group-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupIdentifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socie/latest/actions/add-group-membership', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupIdentifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupIdentifier` | string | yes | The Socie id or externalId of the group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "externalId": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `externalId` | string | The external id for the group membership. |
| `id` | string | The Socie group membership id. |

## Native endpoint

Through the native Socie API, this operation is `POST /api/v1/groups/:groupIdentifier/memberships` (base URL `https://api.socie.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-group-membership.md) for the provider-specific parameters and requirements.

