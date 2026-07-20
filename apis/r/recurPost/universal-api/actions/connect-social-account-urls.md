# RecurPost: Connect Social Account URLs

Retrieves social account connection URLs from RecurPost.

```
GET https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/connect-social-account-urls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RecurPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/connect-social-account-urls?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/connect-social-account-urls?${params}`, {
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
      "message": "string",
      "social_links": [
        {}
      ],
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `social_links` | array<object> |  |
| `status` | number |  |

## Native endpoint

Through the native RecurPost API, this operation is `POST /api/connect_social_account_urls` (base URL `https://social.recurpost.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/connect-social-account-urls.md) for the provider-specific parameters and requirements.

