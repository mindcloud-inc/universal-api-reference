# SmartReach: Create or Update Account

Finds an account in SmartReach, or creates one if needed.

```
POST https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/create-or-update-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/create-or-update-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/create-or-update-account', {
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
| `name` | string | yes | Name of the account |
| `customId` | string | no | custom_id of the account |
| `description` | string | no | description of the account |
| `website` | string | no | website of the account |
| `industry` | string | no | industry of the account |
| `linkedinUrl` | string | no | linkedin_url of the account |
| `customFields` | object | no | custom_fields of the account |
| `updateAccount` | string | no | option for update account |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom_id": "string",
      "id": "string",
      "name": "Ava Chen",
      "team_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_id` | string |  |
| `id` | string |  |
| `name` | string |  |
| `team_id` | string |  |

## Native endpoint

Through the native SmartReach API, this operation is `POST /accounts` (base URL `https://api.smartreach.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-account.md) for the provider-specific parameters and requirements.

