# Benchmark Email: Get Contact Segment

Retrieves a contact segment from Benchmark Email.

```
GET https://connect.mindcloud.co/v1/universal/benchmarkEmail/latest/actions/get-contact-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Benchmark Email `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/benchmarkEmail/latest/actions/get-contact-segment?connectionId=$CONNECTION_ID&segmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "segmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/benchmarkEmail/latest/actions/get-contact-segment?${params}`, {
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
| `segmentId` | string | yes | Benchmark segment ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Benchmark Email API returns.

## Native endpoint

Through the native Benchmark Email API, this operation is `GET /Contact/Segments/:segmentId` (base URL `https://clientapi.benchmarkemail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-segment.md) for the provider-specific parameters and requirements.

