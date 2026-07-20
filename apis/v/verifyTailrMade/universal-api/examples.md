# Verify (Tailr Made) Universal API Examples

These examples use the MindCloud API key and Verify (Tailr Made) connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Resume Red Flags

Analyzes resume text for red flags in Verify.

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

Example response:

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

See the full [Verify Resume Red Flags action reference](actions/verify-resume-red-flags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/verifyTailrMade/latest/actions/verify-resume-red-flags).
