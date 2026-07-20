# Testlify: List Candidate Assessments

Retrieves assessments associated with a specific Testlify candidate.

```
GET https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-candidate-assessments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-candidate-assessments?connectionId=$CONNECTION_ID&candidateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "candidateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-candidate-assessments?${params}`, {
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
| `candidateId` | string | yes | Candidate identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assessmentId": "string",
      "attemptIndex": 1,
      "candidateId": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assessmentId` | string |  |
| `attemptIndex` | number |  |
| `candidateId` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Testlify API, this operation is `GET /v1/assessment/:candidateId/assessments` (base URL `https://api.testlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-candidate-assessments.md) for the provider-specific parameters and requirements.

