# SmartReach: List Accounts

Retrieves accounts from SmartReach.

```
GET https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/list-accounts?${params}`, {
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
| `olderThan` | number | no | timestamp in unix epoch milliseconds |
| `newerThan` | number | no | timestamp in unix epoch milliseconds |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": [
        {
          "id": "string",
          "name": "Ava Chen",
          "team_id": "string"
        }
      ],
      "links": {
        "next": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts[].id` | string |  |
| `accounts[].name` | string |  |
| `accounts[].team_id` | string |  |
| `links.next` | string |  |

## Native endpoint

Through the native SmartReach API, this operation is `GET /accounts` (base URL `https://api.smartreach.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

