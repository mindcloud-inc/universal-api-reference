# Launch27: Get Invite Teams Policy

Retrieves an invite teams policy from Launch27.

```
GET https://connect.mindcloud.co/v1/universal/launch27/latest/actions/get-invite-teams-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch27 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launch27/latest/actions/get-invite-teams-policy?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launch27/latest/actions/get-invite-teams-policy?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "disabled_automatic_actions": [
        "string"
      ],
      "hidden_columns": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `disabled_automatic_actions` | array<string> |  |
| `hidden_columns` | array<string> |  |

## Native endpoint

Through the native Launch27 API, this operation is `GET policy/invite_teams` (base URL `https://{{credentials.subdomain}}.launch27.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invite-teams-policy.md) for the provider-specific parameters and requirements.

