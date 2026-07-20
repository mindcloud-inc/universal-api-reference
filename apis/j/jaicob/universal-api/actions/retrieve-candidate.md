# Jaicob: Retrieve Candidate



```
GET https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/retrieve-candidate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jaicob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/retrieve-candidate?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/retrieve-candidate?${params}`, {
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
| `id` | string | yes | Candidate identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicantDetails": {},
      "certifications": [
        {}
      ],
      "description": "string",
      "educations": [
        {}
      ],
      "function": "string",
      "id": "string",
      "languages": [
        {}
      ],
      "skills": [
        {}
      ],
      "status": "string",
      "tags": [
        "string"
      ],
      "workExperiences": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicantDetails` | object |  |
| `certifications` | array<object> |  |
| `description` | string |  |
| `educations` | array<object> |  |
| `function` | string |  |
| `id` | string |  |
| `languages` | array<object> |  |
| `skills` | array<object> |  |
| `status` | string |  |
| `tags` | array<string> |  |
| `workExperiences` | array<object> |  |

## Native endpoint

Through the native Jaicob API, this operation is `GET /candidates/public/[:id]` (base URL `https://api.jaicob.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-candidate.md) for the provider-specific parameters and requirements.

