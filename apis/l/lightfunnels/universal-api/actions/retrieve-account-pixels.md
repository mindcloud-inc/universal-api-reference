# Lightfunnels: Retrieve Account Pixels



```
GET https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/retrieve-account-pixels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/retrieve-account-pixels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/retrieve-account-pixels?${params}`, {
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
      "account": {
        "facebook_pixels": [
          {}
        ],
        "snapchat_pixels": [
          {}
        ],
        "tiktok_pixels": [
          {}
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object | Account settings root object. |
| `account.facebook_pixels` | array<object> | Configured Facebook pixels. |
| `account.snapchat_pixels` | array<object> | Configured Snapchat pixels. |
| `account.tiktok_pixels` | array<object> | Configured TikTok pixels. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-account-pixels.md) for the provider-specific parameters and requirements.

