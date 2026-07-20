# Fliqr AI: Get Business Account Details

Retrieves business account details from Fliqr AI.

```
GET https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/get-business-account-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fliqr AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/get-business-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/get-business-account-details?${params}`, {
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
      "active": true,
      "created": "string",
      "name": "Ava Chen",
      "pageId": "string",
      "totalUsers": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `created` | string |  |
| `name` | string |  |
| `pageId` | string |  |
| `totalUsers` | string |  |

## Native endpoint

Through the native Fliqr AI API, this operation is `GET /accounts/me` (base URL `https://app.fliqr.ai/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-business-account-details.md) for the provider-specific parameters and requirements.

