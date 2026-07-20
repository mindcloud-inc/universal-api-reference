# Yeti Snow: Get Site Dataprovider



```
GET https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/get-site-dataprovider
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yeti Snow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/get-site-dataprovider?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/get-site-dataprovider?${params}`, {
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
      "area_units": [
        {}
      ],
      "charge_types": [
        {}
      ],
      "countries": [
        {}
      ],
      "measurement_titles": [
        {}
      ],
      "phone_types": [
        {}
      ],
      "provinces": [
        {}
      ],
      "role_types": [
        {}
      ],
      "services": [
        {}
      ],
      "site_notification_types": [
        {}
      ],
      "timezones": [
        {}
      ],
      "weather_enabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `area_units` | array<object> |  |
| `charge_types` | array<object> |  |
| `countries` | array<object> |  |
| `measurement_titles` | array<object> |  |
| `phone_types` | array<object> |  |
| `provinces` | array<object> |  |
| `role_types` | array<object> |  |
| `services` | array<object> |  |
| `site_notification_types` | array<object> |  |
| `timezones` | array<object> |  |
| `weather_enabled` | boolean |  |

## Native endpoint

Through the native Yeti Snow API, this operation is `GET site/dataprovider` (base URL `https://sandbox_api.yetisoftware.com/api/en/public_access/1715`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site-dataprovider.md) for the provider-specific parameters and requirements.

