# Jaicob: Create Candidate



```
POST https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/create-candidate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jaicob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/create-candidate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "applicantDetails": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/create-candidate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "applicantDetails": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `applicantDetails` | object | yes | Candidate identity and contact details. |
| `status` | string | no |  |
| `function` | string | no |  |
| `description` | string | no |  |
| `tags[]` | array<string> | no |  |
| `linkedInSlug` | string | no |  |
| `languages[]` | array<object> | no |  |
| `skills[]` | array<object> | no |  |
| `workExperiences[]` | array<object> | no |  |
| `educations[]` | array<object> | no |  |
| `certifications[]` | array<object> | no |  |
| `locationIds[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Jaicob API, this operation is `POST /candidates` (base URL `https://api.jaicob.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-candidate.md) for the provider-specific parameters and requirements.

