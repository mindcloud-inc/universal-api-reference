# Apideck: Consumer request counts

Retrieves consumer request counts from Apideck Vault.

```
GET https://connect.mindcloud.co/v1/universal/apideck/latest/actions/consumerrequestcountsall
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apideck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apideck/latest/actions/consumerrequestcountsall?connectionId=$CONNECTION_ID&consumer_id=%7B%7Bcredentials.consumerId%7D%7D&start_datetime=string&end_datetime=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "consumer_id": "{{credentials.consumerId}}",
  "start_datetime": "string",
  "end_datetime": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apideck/latest/actions/consumerrequestcountsall?${params}`, {
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
| `consumer_id` | string | yes | Default: `{{credentials.consumerId}}`. |
| `start_datetime` | string | yes |  |
| `end_datetime` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aggregated_request_count": 1,
      "application_id": "string",
      "consumer_id": "string",
      "end_datetime": "string",
      "request_counts": {},
      "start_datetime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aggregated_request_count` | number |  |
| `application_id` | string |  |
| `consumer_id` | string |  |
| `end_datetime` | string |  |
| `request_counts` | object |  |
| `start_datetime` | string |  |

## Native endpoint

Through the native Apideck API, this operation is `GET /vault/consumers/:consumer_id/stats` (base URL `https://unify.apideck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/consumerrequestcountsall.md) for the provider-specific parameters and requirements.

