# Scalr: Get Service Account

Retrieves a service account from Scalr.

```
GET https://connect.mindcloud.co/v1/universal/scalr/latest/actions/get-service-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scalr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scalr/latest/actions/get-service-account?connectionId=$CONNECTION_ID&service_account=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "service_account": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scalr/latest/actions/get-service-account?${params}`, {
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
| `service_account` | string | yes | Scalr service account ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Scalr API returns.

## Native endpoint

Through the native Scalr API, this operation is `GET /service-accounts/:service_account` (base URL `https://mindcloud.scalr.io/api/iacp/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service-account.md) for the provider-specific parameters and requirements.

