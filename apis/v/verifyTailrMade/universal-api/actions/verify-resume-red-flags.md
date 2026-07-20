# Verify (Tailr Made): Verify Resume Red Flags

Analyzes resume text for red flags in Verify.

```
GET https://connect.mindcloud.co/v1/universal/verifyTailrMade/latest/actions/verify-resume-red-flags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verify (Tailr Made) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verifyTailrMade/latest/actions/verify-resume-red-flags?connectionId=$CONNECTION_ID&resumeText=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resumeText": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verifyTailrMade/latest/actions/verify-resume-red-flags?${params}`, {
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
| `resumeText` | string | yes | Text to analyze for red flags and fraud signals. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analysis": {
        "flags": {
          "employers": [
            "string"
          ],
          "schools": [
            "string"
          ],
          "tech": [
            "string"
          ]
        },
        "resumeData": {
          "experience": {
            "employerRecognition": {},
            "parsedExperience": [
              "string"
            ]
          },
          "fullText": "string",
          "linkedInUrl": "https://example.com",
          "name": "Ava Chen",
          "schools": [
            "string"
          ],
          "tech": [
            "string"
          ]
        }
      },
      "reportHTML": "string",
      "reportText": "string",
      "riskLevel": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analysis` | object | Structured analysis payload. |
| `analysis.flags` | object | High-level analysis flags. |
| `analysis.flags.employers` | array |  |
| `analysis.flags.schools` | array |  |
| `analysis.flags.tech` | array |  |
| `analysis.resumeData` | object | Normalized resume data used by the analysis. |
| `analysis.resumeData.experience` | object | Parsed experience metadata. |
| `analysis.resumeData.experience.employerRecognition` | object | Employer recognition map. |
| `analysis.resumeData.experience.parsedExperience` | array |  |
| `analysis.resumeData.fullText` | string | Resume text sent for analysis. |
| `analysis.resumeData.linkedInUrl` | string | Parsed LinkedIn URL, when available. |
| `analysis.resumeData.name` | string | Parsed candidate name, when available. |
| `analysis.resumeData.schools` | array |  |
| `analysis.resumeData.tech` | array |  |
| `reportHTML` | string | HTML verify report. |
| `reportText` | string | Plain-text verify report. |
| `riskLevel` | string | Overall risk level returned by the verify endpoint. |

## Native endpoint

Through the native Verify (Tailr Made) API, this operation is `POST /api/verify` (base URL `https://api.tailrmadeai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-resume-red-flags.md) for the provider-specific parameters and requirements.

