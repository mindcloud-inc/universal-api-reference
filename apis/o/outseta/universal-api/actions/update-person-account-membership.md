# Outseta: Update Person Account Membership

Updates an existing account membership in Outseta.

```
PUT https://connect.mindcloud.co/v1/universal/outseta/latest/actions/update-person-account-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outseta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/update-person-account-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountUid": "string",
  "membershipUid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outseta/latest/actions/update-person-account-membership', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountUid": "string",
    "membershipUid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountUid` | string | yes |  |
| `membershipUid` | string | yes |  |
| `person.uid` | string | no |  |
| `isPrimary` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Account": "string",
      "Created": "string",
      "IsPrimary": true,
      "Person": "string",
      "Uid": "string",
      "Updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Account` | string |  |
| `Created` | string |  |
| `IsPrimary` | boolean |  |
| `Person` | string |  |
| `Uid` | string |  |
| `Updated` | string |  |

## Native endpoint

Through the native Outseta API, this operation is `PUT /crm/accounts/:accountUid/memberships/:membershipUid` (base URL `https://{{credentials.subdomain}}.outseta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-person-account-membership.md) for the provider-specific parameters and requirements.

