# Lightfunnels: Update Account Pixels



```
PUT https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/update-account-pixels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/update-account-pixels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/update-account-pixels', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "updateAccount": {
        "facebookPixels": [
          {
            "label": "string",
            "value": "string"
          }
        ],
        "snapchatPixels": [
          {}
        ],
        "tiktokPixels": [
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
| `updateAccount` | object | Updated account settings. |
| `updateAccount.facebookPixels` | array<object> | Facebook pixels. |
| `updateAccount.facebookPixels[].label` | string | Pixel label. |
| `updateAccount.facebookPixels[].value` | string | Pixel value. |
| `updateAccount.snapchatPixels` | array<object> | Snapchat pixels. |
| `updateAccount.tiktokPixels` | array<object> | TikTok pixels. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-account-pixels.md) for the provider-specific parameters and requirements.

