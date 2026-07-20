# Pilvio: Get S3 User



```
GET https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/get-s3-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pilvio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/get-s3-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/get-s3-user?${params}`, {
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
      "caps": [
        "string"
      ],
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "maxBuckets": 1,
      "s3Credentials": [
        {
          "accessKey": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `caps` | array<string> |  |
| `displayName` | string |  |
| `email` | string |  |
| `maxBuckets` | number |  |
| `s3Credentials[].accessKey` | string |  |

## Native endpoint

Through the native Pilvio API, this operation is `GET /storage/user` (base URL `https://api.pilvio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-s3-user.md) for the provider-specific parameters and requirements.

