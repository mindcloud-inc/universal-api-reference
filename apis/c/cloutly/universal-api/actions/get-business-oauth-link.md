# Cloutly: Get Business OAuth Link

Retrieves a business source auth link from Cloutly.

```
GET https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/get-business-oauth-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloutly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/get-business-oauth-link?connectionId=$CONNECTION_ID&businessId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/get-business-oauth-link?${params}`, {
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
| `businessId` | string | yes | Business ID from Cloutly. |
| `logoSrc` | string | no | Logo URL shown during provider connection. |
| `redirect` | string | no | URL to send the user back to after OAuth. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cloutly API returns.

## Native endpoint

Through the native Cloutly API, this operation is `POST https://marketplace.cloutly.com/api/v2/businesses/:businessId/auth-link` (base URL `https://app.cloutly.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-business-oauth-link.md) for the provider-specific parameters and requirements.

