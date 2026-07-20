# Jaicob: Parse Resume



```
GET https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/parse-resume
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jaicob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/parse-resume?connectionId=$CONNECTION_ID&resume=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resume": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/parse-resume?${params}`, {
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
| `requestId` | string | no | Optional idempotency or trace identifier. |
| `resume` | file | yes | Resume file to parse. |

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
      "companyId": "string",
      "description": "string",
      "educations": [
        {}
      ],
      "function": "string",
      "languages": [
        {}
      ],
      "linkedInSlug": "https://example.com",
      "resumeUrl": "https://example.com",
      "skills": [
        {}
      ],
      "tags": [
        "string"
      ],
      "userId": "string",
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
| `companyId` | string |  |
| `description` | string |  |
| `educations` | array<object> |  |
| `function` | string |  |
| `languages` | array<object> |  |
| `linkedInSlug` | string |  |
| `resumeUrl` | string |  |
| `skills` | array<object> |  |
| `tags` | array<string> |  |
| `userId` | string |  |
| `workExperiences` | array<object> |  |

## Native endpoint

Through the native Jaicob API, this operation is `POST /file/resume` (base URL `https://api.jaicob.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-resume.md) for the provider-specific parameters and requirements.

