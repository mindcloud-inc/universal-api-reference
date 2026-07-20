# Intradesk: Search Clients

Finds clients in Intradesk by email or phone.

```
GET https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/search-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/search-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/search-clients?${params}`, {
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
| `email` | string | no | Client email search filter. |
| `phone` | string | no | Client phone search filter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `top` | number | no | Maximum number of clients to return. Defaults to 50 in Intradesk docs. |
| `isIncludeArchived` | boolean | no | Whether archived clients should be included. Defaults to false in Intradesk docs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | number |  |
| `userId` | number |  |

## Native endpoint

Through the native Intradesk API, this operation is `GET /settings/api/v1/clients/Search` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-clients.md) for the provider-specific parameters and requirements.

