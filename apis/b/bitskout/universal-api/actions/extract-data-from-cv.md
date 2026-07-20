# Bitskout: Extract Data from CV

Extracts CV data with a Bitskout plugin.

```
POST https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-data-from-cv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitskout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-data-from-cv" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-data-from-cv', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileUrl` | string | no | Direct download URL for the resume file to extract. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "outputs": {
        "EDUCATION": "string",
        "EMAILS": "ava@example.com",
        "EXPERIENCE": "string",
        "JOB_TITLE": "string",
        "LINKEDIN": "https://example.com",
        "LOCATION": "string",
        "NAME": "Ava Chen",
        "PHONE_NUMBERS": "string",
        "RawJSON": "string",
        "SKILLS": "string",
        "TOTAL_YEARS_EXPERIENCE": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `outputs` | object | Resume extraction outputs |
| `outputs.EDUCATION` | string | Education |
| `outputs.EMAILS` | string | List of emails specified in the resume |
| `outputs.EXPERIENCE` | string | Experience |
| `outputs.JOB_TITLE` | string | Job Title |
| `outputs.LINKEDIN` | string | LinkedIn Profile |
| `outputs.LOCATION` | string | Location |
| `outputs.NAME` | string | Person's name |
| `outputs.PHONE_NUMBERS` | string | List of phone numbers |
| `outputs.RawJSON` | string | Raw JSON |
| `outputs.SKILLS` | string | List of Skills |
| `outputs.TOTAL_YEARS_EXPERIENCE` | string | Total years of experience |

## Native endpoint

Through the native Bitskout API, this operation is `POST /actions/cv` (base URL `https://api.bitskout.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-data-from-cv.md) for the provider-specific parameters and requirements.

