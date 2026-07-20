# Forminit: Submit Form

Creates a new submission for a Forminit form.

```
POST https://connect.mindcloud.co/v1/universal/forminit/latest/actions/submit-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Forminit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/forminit/latest/actions/submit-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "kua953xaju5",
  "blocks": "[object Object],[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/forminit/latest/actions/submit-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "kua953xaju5",
    "blocks": "[object Object],[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The Forminit form identifier. Example: `kua953xaju5`. |
| `blocks` | string<string> | yes | JSON string containing the Forminit `blocks` array. Example: `[object Object],[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "redirectUrl": "https://example.com",
      "submission": {
        "blocks": {},
        "date": "string",
        "hashId": "string",
        "submissionInfo": {
          "ip": "string",
          "location": {
            "city": {
              "name": "Ava Chen"
            },
            "country": {
              "iso": "string",
              "name": "Ava Chen"
            },
            "geo": {
              "lat": 1,
              "lng": 1
            },
            "timezone": "string"
          },
          "referer": "string",
          "sdk_version": "string",
          "user_agent": "string"
        }
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `redirectUrl` | string | Redirect URL returned after successful submission. |
| `submission` | object | Created submission details. |
| `submission.blocks` | object |  |
| `submission.date` | string |  |
| `submission.hashId` | string |  |
| `submission.submissionInfo` | object |  |
| `submission.submissionInfo.ip` | string |  |
| `submission.submissionInfo.location` | object |  |
| `submission.submissionInfo.location.city.name` | string |  |
| `submission.submissionInfo.location.country.iso` | string |  |
| `submission.submissionInfo.location.country.name` | string |  |
| `submission.submissionInfo.location.geo.lat` | number |  |
| `submission.submissionInfo.location.geo.lng` | number |  |
| `submission.submissionInfo.location.timezone` | string |  |
| `submission.submissionInfo.referer` | string |  |
| `submission.submissionInfo.sdk_version` | string |  |
| `submission.submissionInfo.user_agent` | string |  |
| `success` | boolean | Whether the submission was accepted by Forminit. |

## Native endpoint

Through the native Forminit API, this operation is `POST /f/:formId` (base URL `https://api.forminit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-form.md) for the provider-specific parameters and requirements.

