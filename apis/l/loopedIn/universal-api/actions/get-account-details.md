# LoopedIn: Get Account Details

Retrieves account details from LoopedIn.

```
GET https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/get-account-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoopedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/get-account-details?${params}`, {
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
      "announcementCategories": [
        {}
      ],
      "created": "string",
      "feedbackCategories": [
        {}
      ],
      "id": "string",
      "ideaCategories": [
        {}
      ],
      "objectives": [
        {}
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `announcementCategories` | array<object> |  |
| `created` | string |  |
| `feedbackCategories` | array<object> |  |
| `id` | string |  |
| `ideaCategories` | array<object> |  |
| `objectives` | array<object> |  |
| `title` | string |  |

## Native endpoint

Through the native LoopedIn API, this operation is `GET /account` (base URL `https://api.loopedin.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-details.md) for the provider-specific parameters and requirements.

