# IntakeQ: Download Intake Consent PDF

Retrieves an intake consent PDF from IntakeQ.

```
GET https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/download-intake-consent-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/download-intake-consent-pdf?connectionId=$CONNECTION_ID&intakeId=string&consentFormId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "intakeId": "string",
  "consentFormId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/download-intake-consent-pdf?${params}`, {
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
| `intakeId` | string | yes | The IntakeQ intake form ID. |
| `consentFormId` | string | yes | The consent form ID associated with the intake. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "data": "string",
      "fileName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `data` | string |  |
| `fileName` | string |  |

## Native endpoint

Through the native IntakeQ API, this operation is `GET /intakes/{intakeId}/consent/{consentFormId}/pdf` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-intake-consent-pdf.md) for the provider-specific parameters and requirements.

