# Bookafy: List Services with Details

Retrieves services with details from Bookafy.

```
GET https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/list-services-with-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookafy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/list-services-with-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/list-services-with-details?${params}`, {
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
      "response": {
        "services": [
          {
            "categoryId": 1,
            "clientId": 1,
            "createdAt": "2026-05-07T12:00:00.000Z",
            "duration": "string",
            "forClient": true,
            "id": 1,
            "isChargeable": true,
            "price": "string",
            "schedulingMode": "string",
            "serviceName": "Ava Chen",
            "slug": "string",
            "updatedAt": "2026-05-07T12:00:00.000Z"
          }
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
| `response.services[].categoryId` | number | Service category ID. |
| `response.services[].clientId` | number | Owning Bookafy client ID. |
| `response.services[].createdAt` | date | Service creation timestamp. |
| `response.services[].duration` | string | Service duration in minutes. |
| `response.services[].forClient` | boolean | Whether the service is available to clients. |
| `response.services[].id` | number | Service ID. |
| `response.services[].isChargeable` | boolean | Whether the service is chargeable. |
| `response.services[].price` | string | Service price. |
| `response.services[].schedulingMode` | string | Scheduling mode for the service. |
| `response.services[].serviceName` | string | Service display name. |
| `response.services[].slug` | string | Service slug used in booking links. |
| `response.services[].updatedAt` | date | Service update timestamp. |

## Native endpoint

Through the native Bookafy API, this operation is `GET /services` (base URL `https://app.bookafy.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-services-with-details.md) for the provider-specific parameters and requirements.

