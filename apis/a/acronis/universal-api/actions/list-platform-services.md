# Acronis: List Platform Services

Retrieves all platform services from Acronis.

```
GET https://connect.mindcloud.co/v1/universal/acronis/latest/actions/list-platform-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acronis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acronis/latest/actions/list-platform-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acronis/latest/actions/list-platform-services?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Acronis API returns.

## Native endpoint

Through the native Acronis API, this operation is `GET /api/2/applications` (base URL `{{credentials.dataCenterUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-platform-services.md) for the provider-specific parameters and requirements.

