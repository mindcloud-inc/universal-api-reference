# Dotdigital: Get Account Information

Retrieves account status information from Dotdigital.

```
GET https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-account-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dotdigital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-account-information?${params}`, {
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
      "id": 1,
      "properties": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | The dotdigital account identifier. |
| `properties[]` | array<object> | Account properties returned by dotdigital. |
| `properties[].name` | string | The property name. |
| `properties[].type` | string | The property type. |
| `properties[].value` | string | The property value as returned by dotdigital. |

## Native endpoint

Through the native Dotdigital API, this operation is `GET /v2/account-info` (base URL `https://r2-api.dotmailer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-information.md) for the provider-specific parameters and requirements.

