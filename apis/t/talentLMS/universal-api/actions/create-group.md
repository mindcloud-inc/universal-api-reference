# TalentLMS: Create Group

Creates a new group in TalentLMS.

```
POST https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/create-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentLMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/create-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/create-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Group name. |
| `description` | string | no | Group description. |
| `key` | string | no | Group redemption key. |
| `maxKeyRedemptions` | number | no | Maximum key redemptions. |
| `price` | number | no | Group price. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branch": {},
      "description": "string",
      "id": 1,
      "key": "string",
      "maxKeyRedemptions": 1,
      "name": "Ava Chen",
      "price": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branch` | object |  |
| `description` | string |  |
| `id` | number |  |
| `key` | string |  |
| `maxKeyRedemptions` | number |  |
| `name` | string |  |
| `price` | object |  |

## Native endpoint

Through the native TalentLMS API, this operation is `POST /groups` (base URL `https://{{credentials.domain}}.talentlms.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group.md) for the provider-specific parameters and requirements.

