# Typless: List Awaiting Poll Extractions



```
GET https://connect.mindcloud.co/v1/universal/typless/latest/actions/list-awaiting-poll-extractions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typless/latest/actions/list-awaiting-poll-extractions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typless/latest/actions/list-awaiting-poll-extractions?${params}`, {
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
| `customer` | string | no | Optional customer identifier to scope the awaiting poll queue. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extraction_ids": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extraction_ids` | array<string> | List of pending Typless extraction job IDs waiting to be polled. |

## Native endpoint

Through the native Typless API, this operation is `GET /api/v1/awaiting-poll` (base URL `https://developers.typless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-awaiting-poll-extractions.md) for the provider-specific parameters and requirements.

