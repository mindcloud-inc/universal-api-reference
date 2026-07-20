# Host.io: Get Domain Full Details

Retrieves full domain details from Host.io.

```
GET https://connect.mindcloud.co/v1/universal/hostio/latest/actions/get-domain-full-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Host.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hostio/latest/actions/get-domain-full-details?connectionId=$CONNECTION_ID&domain=google.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "google.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hostio/latest/actions/get-domain-full-details?${params}`, {
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
| `domain` | string | yes | Domain to look up with Host.io full domain details. Default: `google.com`. Example: `google.com`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Host.io API returns.

## Native endpoint

Through the native Host.io API, this operation is `GET /full/:domain` (base URL `https://host.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-full-details.md) for the provider-specific parameters and requirements.

