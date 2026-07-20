# ForceManager: Read Opportunities

Retrieves opportunities from your ForceManager account.

```
GET https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/read-opportunities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ForceManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/read-opportunities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/read-opportunities?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "amount": 1,
      "closingDateExpected": "2026-05-07T12:00:00.000Z",
      "comments": "string",
      "id": 1,
      "probability": 1,
      "topic": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Address line 1 of the opportunity. |
| `amount` | number | Amount of the opportunity. |
| `closingDateExpected` | date | Expected closing date of the opportunity. |
| `comments` | string | Comments for the opportunity. |
| `id` | number | Unique identifier for the opportunity. |
| `probability` | number | Probability of the opportunity. |
| `topic` | string | Topic of the opportunity. |

## Native endpoint

Through the native ForceManager API, this operation is `GET /opportunities`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-opportunities.md) for the provider-specific parameters and requirements.

