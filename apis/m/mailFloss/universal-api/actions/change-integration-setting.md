# MailFloss: Change Integration Setting

Updates an integration setting in MailFloss.

```
PUT https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/change-integration-setting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailFloss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/change-integration-setting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/change-integration-setting', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Integration setting ID. |
| `id` | string | yes | Integration ID to update. |
| `type` | string | yes | Setting type to modify. MailFloss documents whitelist, blacklist, aggressiveness, frequency, or action. |
| `data.keyword` | string | no | Keyword used for blacklist or whitelist insertion. |
| `data.processed` | boolean | no | Whether the job has finished processing. |
| `data.localpart` | boolean | no | Use the localpart for blacklist or whitelist insertion. |
| `data.domain` | boolean | no | Use the domain for blacklist or whitelist insertion. |
| `data.email` | boolean | no | Use the whole email address for blacklist or whitelist insertion. |
| `data.match` | string | no | Match type. MailFloss documents exact or contains. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Success status for the integration setting change. |

## Native endpoint

Through the native MailFloss API, this operation is `POST /settings/:id` (base URL `https://api.mailfloss.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-integration-setting.md) for the provider-specific parameters and requirements.

