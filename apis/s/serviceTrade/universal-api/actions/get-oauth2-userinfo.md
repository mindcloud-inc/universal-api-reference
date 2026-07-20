# ServiceTrade: Get OAuth2 Userinfo



```
GET https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/get-oauth2-userinfo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTrade `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/get-oauth2-userinfo?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/get-oauth2-userinfo?${params}`, {
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
        "id": 1,
        "name": "Ava Chen",
        "uri": "string"
      },
      "clientId": "string",
      "company": {
        "id": 1,
        "name": "Ava Chen",
        "status": "string",
        "uri": "string"
      },
      "environment": "string",
      "isDemo": true,
      "name": "Ava Chen",
      "status": "string",
      "timezone": "string",
      "type": "string",
      "uri": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.id` | number |  |
| `account.name` | string |  |
| `account.uri` | string |  |
| `clientId` | string |  |
| `company.id` | number |  |
| `company.name` | string |  |
| `company.status` | string |  |
| `company.uri` | string |  |
| `environment` | string |  |
| `isDemo` | boolean |  |
| `name` | string |  |
| `status` | string |  |
| `timezone` | string |  |
| `type` | string |  |
| `uri` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native ServiceTrade API, this operation is `GET oauth2/userinfo` (base URL `https://api.servicetrade.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-oauth2-userinfo.md) for the provider-specific parameters and requirements.

