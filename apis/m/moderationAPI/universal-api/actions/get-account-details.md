# Moderation API: Get Account Details

Retrieves account details from Moderation API.

```
GET https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-account-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moderation API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-account-details?${params}`, {
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
      "current_project": {},
      "id": "string",
      "paid_plan_name": "Ava Chen",
      "remaining_quota": 1,
      "text_api_quota": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_project` | object |  |
| `id` | string | ID of the account |
| `paid_plan_name` | string | Name of the paid plan |
| `remaining_quota` | number | Remaining quota |
| `text_api_quota` | number | Text API quota |

## Native endpoint

Through the native Moderation API API, this operation is `GET /account` (base URL `https://api.moderationapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-details.md) for the provider-specific parameters and requirements.

