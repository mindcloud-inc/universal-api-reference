# DocuPanda - Document Understanding: Match a standardization to a list of candidates

Creates a standardization match in DocuPanda.

```
POST https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/match-standardization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/match-standardization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "instructions": "string",
  "matchCandidates": "string",
  "standardizationId": "string",
  "matchCandidates[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/match-standardization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "instructions": "string",
    "matchCandidates": "string",
    "standardizationId": "string",
    "matchCandidates[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `instructions` | string | yes | The instructions for the match |
| `matchCandidates` | list<string> | yes |  |
| `standardizationId` | string | yes | The id of the standardization you're looking to match |
| `matchCandidates[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "matchingRecords": [
        "string"
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
| `matchingRecords` | array<string> | The records that matched in descending order of likelihood. Usually one record |
| `reasoning` | string | The reasoning behind the match |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /enterprise/matching` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/match-standardization.md) for the provider-specific parameters and requirements.

