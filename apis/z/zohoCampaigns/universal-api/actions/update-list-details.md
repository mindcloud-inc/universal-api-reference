# Zoho Campaigns: Update List Details

Updates a Zoho Campaigns mailing list.

```
PUT https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/update-list-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Campaigns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/update-list-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listKey": "string",
  "newListName": "Ava Chen",
  "signupForm": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/update-list-details', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listKey": "string",
    "newListName": "Ava Chen",
    "signupForm": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listKey` | list<string> | yes | List key to update. |
| `newListName` | string | yes | New name to apply to the mailing list. |
| `signupForm` | string | yes | Whether the mailing list signup form stays public or private. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "message": "string",
      "status": "string",
      "uri": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Zoho result code. |
| `message` | string | Provider message for the list update. |
| `status` | string | Zoho status string. |
| `uri` | string | Zoho endpoint URI. |
| `version` | string | Zoho API version. |

## Native endpoint

Through the native Zoho Campaigns API, this operation is `POST /updatelistdetails` (base URL `https://campaigns.zoho.com/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-list-details.md) for the provider-specific parameters and requirements.

