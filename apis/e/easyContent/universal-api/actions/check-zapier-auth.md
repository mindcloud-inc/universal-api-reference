# EasyContent: Check Zapier Auth

Checks an EasyContent Zapier API key and returns its account.

```
GET https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/check-zapier-auth
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/check-zapier-auth?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/check-zapier-auth?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EasyContent API returns.

## Native endpoint

Through the native EasyContent API, this operation is `GET /zapier/auth` (base URL `https://easycontent.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-zapier-auth.md) for the provider-specific parameters and requirements.

