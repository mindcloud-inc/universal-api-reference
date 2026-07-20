# Cerbo: Create Patient Image

Creates a new patient image in Cerbo.

```
POST https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-patient-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-patient-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pt_id": 1,
  "mime_type": "string",
  "base64_content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-patient-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pt_id": 1,
    "mime_type": "string",
    "base64_content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `patient_id` | number | no | ID of patient |
| `pt_id` | number | yes | An integer identifier for the patient associated with the document. |
| `mime_type` | string | yes | A string indicating the MIME type of the file. Valid MIME types: image/jpeg image/jpg image/gif image/png image/pngx |
| `base64_content` | string | yes | Binary data, encoded base64. Maximum file size is 16MB. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `POST /patients/:patient_id/images` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-patient-image.md) for the provider-specific parameters and requirements.

