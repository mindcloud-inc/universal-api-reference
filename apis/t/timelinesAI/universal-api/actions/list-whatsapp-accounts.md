# TimelinesAI: List WhatsApp Accounts

Retrieves WhatsApp accounts connected in TimelinesAI.

```
GET https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-whatsapp-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimelinesAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-whatsapp-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-whatsapp-accounts?${params}`, {
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
      "data": {
        "whatsappAccounts": [
          {
            "accountName": "Ava Chen",
            "connectedOn": "string",
            "id": "string",
            "ownerEmail": "ava@example.com",
            "ownerName": "Ava Chen",
            "phone": "string",
            "status": "string"
          }
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.whatsappAccounts` | array<object> |  |
| `data.whatsappAccounts[].accountName` | string |  |
| `data.whatsappAccounts[].connectedOn` | string |  |
| `data.whatsappAccounts[].id` | string |  |
| `data.whatsappAccounts[].ownerEmail` | string |  |
| `data.whatsappAccounts[].ownerName` | string |  |
| `data.whatsappAccounts[].phone` | string |  |
| `data.whatsappAccounts[].status` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TimelinesAI API, this operation is `GET /whatsapp_accounts` (base URL `https://app.timelines.ai/integrations/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-whatsapp-accounts.md) for the provider-specific parameters and requirements.

