# Satiurn: Get Labels

Retrieves labels from Satiurn.

```
GET https://connect.mindcloud.co/v1/universal/satiurn/latest/actions/get-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Satiurn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/satiurn/latest/actions/get-labels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/satiurn/latest/actions/get-labels?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Satiurn API returns.

## Native endpoint

Through the native Satiurn API, this operation is `GET /label/labels` (base URL `https://publicapi.satiurn.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-labels.md) for the provider-specific parameters and requirements.

