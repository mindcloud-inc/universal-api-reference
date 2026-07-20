# PostcardMania: Get Batch

Retrieves a batch from PostcardMania.

```
GET https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/get-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/get-batch?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/get-batch?${params}`, {
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
| `batchID` | string | no | Numeric PostcardMania batch identifier. |
| `batchID` | string | no | The batch identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchID` | number | Batch identifier. |

## Native endpoint

Through the native PostcardMania API, this operation is `GET /batch/{{batchID}}` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch.md) for the provider-specific parameters and requirements.

