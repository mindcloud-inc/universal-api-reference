# DocuPipe: Match a standardization to a list of candidates

Matches a standardization to candidates in DocuPipe.

```
POST https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/match-a-standardization-to-a-list-of-candidates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/match-a-standardization-to-a-list-of-candidates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "standardizationId": "string",
  "matchCandidates[]": [
    {}
  ],
  "instructions": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/match-a-standardization-to-a-list-of-candidates', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "standardizationId": "string",
    "matchCandidates[]": [{}],
    "instructions": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `standardizationId` | string | yes | The id of the standardization you're looking to match |
| `matchCandidates[]` | array<object> | yes |  |
| `instructions` | string | yes | The instructions for the match |

## Response

```json
{
  "success": true,
  "data": [
    {
      "matchingRecords": [
        {}
      ],
      "reasoning": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `matchingRecords` | array<object> | The records that matched in descending order of likelihood. Usually one record |
| `reasoning` | string | The reasoning behind the match |

## Native endpoint

Through the native DocuPipe API, this operation is `POST /enterprise/matching` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/match-a-standardization-to-a-list-of-candidates.md) for the provider-specific parameters and requirements.

