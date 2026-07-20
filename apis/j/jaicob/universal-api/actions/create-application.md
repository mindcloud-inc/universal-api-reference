# Jaicob: Create Application



```
POST https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/create-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jaicob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/create-application" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "vacancyId": "string",
  "applicantDetails": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/create-application', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "vacancyId": "string",
    "applicantDetails": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vacancyId` | string | yes | Vacancy identifier. |
| `applicantDetails` | object | yes | Applicant identity and contact details. |
| `function` | string | no |  |
| `description` | string | no |  |
| `resumeUrl` | string | no |  |
| `workExperiences[]` | array<object> | no |  |
| `educations[]` | array<object> | no |  |
| `certifications[]` | array<object> | no |  |
| `appliedWith` | string | no |  |
| `coverLetter` | string | no |  |
| `remarks` | string | no |  |

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

Through the native Jaicob API, this operation is `POST /applications/[:vacancyId]` (base URL `https://api.jaicob.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-application.md) for the provider-specific parameters and requirements.

