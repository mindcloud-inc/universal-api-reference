# CardClan: List Email Accounts

Retrieves email accounts configured in CardClan workspaces.

```
GET https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/list-email-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CardClan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/list-email-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/list-email-accounts?${params}`, {
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
      "_id": "string",
      "choices": [
        {}
      ],
      "key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | Owning CardClan user ID for the email-account choice set. |
| `choices` | array<object> | Available sender email-account choices. |
| `key` | string | Response group key. |

## Native endpoint

Through the native CardClan API, this operation is `GET /integration/email-accounts` (base URL `https://app.cardclan.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-email-accounts.md) for the provider-specific parameters and requirements.

