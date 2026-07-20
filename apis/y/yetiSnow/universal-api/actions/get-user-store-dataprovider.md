# Yeti Snow: Get User Store Dataprovider



```
GET https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/get-user-store-dataprovider
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yeti Snow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/get-user-store-dataprovider?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/get-user-store-dataprovider?${params}`, {
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
      "countries": [
        {}
      ],
      "phone_types": [
        {}
      ],
      "provinces": [
        {}
      ],
      "timezones": [
        {}
      ],
      "user_types": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countries` | array<object> |  |
| `phone_types` | array<object> |  |
| `provinces` | array<object> |  |
| `timezones` | array<object> |  |
| `user_types` | array<object> |  |

## Native endpoint

Through the native Yeti Snow API, this operation is `GET user/store_dataprovider` (base URL `https://sandbox_api.yetisoftware.com/api/en/public_access/1715`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-store-dataprovider.md) for the provider-specific parameters and requirements.

