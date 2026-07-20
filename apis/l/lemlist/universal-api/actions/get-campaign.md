# lemlist: Get Campaign

Retrieves a specific campaign from lemlist.

```
GET https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lemlist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/get-campaign?connectionId=$CONNECTION_ID&campaignId=67618ad126d28d06429eb1c4" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "67618ad126d28d06429eb1c4"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/get-campaign?${params}`, {
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
| `campaignId` | string | yes | The ID of the campaign to retrieve. Example: `67618ad126d28d06429eb1c4`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "creator": {
        "userEmail": "ava@example.com",
        "userId": "string"
      },
      "id": "string",
      "name": "Ava Chen",
      "senders": [
        "string"
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `creator` | object |  |
| `creator.userEmail` | string |  |
| `creator.userId` | string |  |
| `id` | string |  |
| `name` | string |  |
| `senders` | array<string> |  |
| `status` | string |  |

## Native endpoint

Through the native lemlist API, this operation is `GET /campaigns/:campaignId` (base URL `https://api.lemlist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

