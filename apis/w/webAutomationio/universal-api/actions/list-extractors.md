# WebAutomation.io: List Extractors

Lists all extractors in your WebAutomation account.

```
GET https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/list-extractors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebAutomation.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/list-extractors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/list-extractors?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WebAutomation.io API returns.

## Native endpoint

Through the native WebAutomation.io API, this operation is `GET /extractors/` (base URL `https://webautomation.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-extractors.md) for the provider-specific parameters and requirements.

