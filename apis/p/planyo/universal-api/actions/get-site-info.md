# Planyo: Get Site Info

Retrieves site information from Planyo.

```
GET https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-site-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planyo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-site-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-site-info?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | number | no | Optional site ID for metasite API keys. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeExtensions": [
        {}
      ],
      "adminId": "string",
      "category": "string",
      "customResourceProperties": [
        {}
      ],
      "dateFormat": "string",
      "defaultLanguage": "string",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "onlinePaymentSurcharge": 1,
      "photos": [
        {}
      ],
      "properties": {},
      "timezone": "string",
      "timezoneOffset": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeExtensions` | array<object> |  |
| `adminId` | string |  |
| `category` | string |  |
| `customResourceProperties` | array<object> |  |
| `dateFormat` | string |  |
| `defaultLanguage` | string |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `onlinePaymentSurcharge` | number |  |
| `photos` | array<object> |  |
| `properties` | object |  |
| `timezone` | string |  |
| `timezoneOffset` | string |  |

## Native endpoint

Through the native Planyo API, this operation is `GET /` (base URL `https://www.planyo.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site-info.md) for the provider-specific parameters and requirements.

