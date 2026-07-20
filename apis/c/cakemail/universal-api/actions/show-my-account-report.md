# Cakemail: Show My Account Report

Retrieves the current account report from Cakemail.

```
GET https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/show-my-account-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cakemail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/show-my-account-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/show-my-account-report?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cakemail API returns.

## Native endpoint

Through the native Cakemail API, this operation is `GET /reports/accounts/self` (base URL `https://api.cakemail.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-my-account-report.md) for the provider-specific parameters and requirements.

