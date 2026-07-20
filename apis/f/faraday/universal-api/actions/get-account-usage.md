# Faraday: Get Account Usage

Retrieves account usage metrics from Faraday.

```
GET https://connect.mindcloud.co/v1/universal/faraday/latest/actions/get-account-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Faraday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/faraday/latest/actions/get-account-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/faraday/latest/actions/get-account-usage?${params}`, {
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
| `account_id` | string | no | Faraday account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "finishedAt": "string",
      "id": "string",
      "startedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `finishedAt` | string | Usage window end. |
| `id` | string | Account ID. |
| `startedAt` | string | Usage window start. |

## Native endpoint

Through the native Faraday API, this operation is `GET /accounts/:account_id/usage` (base URL `https://api.faraday.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-usage.md) for the provider-specific parameters and requirements.

