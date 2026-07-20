# GetSales.io: Get Sender Profile



```
GET https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/get-sender-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetSales.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/get-sender-profile?connectionId=$CONNECTION_ID&senderProfileUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "senderProfileUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/get-sender-profile?${params}`, {
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
| `senderProfileUuid` | string | yes | UUID of the sender profile to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee_user_id": 1,
      "first_name": "Ava",
      "label": "string",
      "last_name": "Chen",
      "status": "string",
      "team_id": 1,
      "user_id": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee_user_id` | number |  |
| `first_name` | string |  |
| `label` | string |  |
| `last_name` | string |  |
| `status` | string |  |
| `team_id` | number |  |
| `user_id` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native GetSales.io API, this operation is `GET /flows/api/sender-profiles/{senderProfileUuid}` (base URL `https://amazing.getsales.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sender-profile.md) for the provider-specific parameters and requirements.

