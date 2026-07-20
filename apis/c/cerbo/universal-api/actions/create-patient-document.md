# Cerbo: Create Patient Document

Creates a new patient document in Cerbo.

```
POST https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-patient-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-patient-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-patient-document', {
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
| `patient_id` | number | no | ID of patient |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `enqueue` | boolean | no | (true by default) If true, the system will insert the document into the active patient portal queue so that the clinic is notified and can review the proposed addition |
| `pt_id` | number | no | (required) An integer identifier for the patient associated with the document. |
| `mime_type` | string | no | (required) A string indicating the MIME type of the file. |
| `name` | string | no | (required) A string to be used as the title of the document. |
| `base64_content` | string | no | (required) Binary data, encoded base64. Maximum file size is 16MB. |
| `notes` | string | no | (optional, enqueue=true only) A string to provide highlights or context about the document submission request when document is being enqueued (if accepted from the queue, this will get added to the document `content` section) |
| `content` | string | no | (optional, enqueue=false only) A string to provide highlights or context about the document when document is being injected directly into the patient chart (enqueue=false) |
| `folder` | string | no | (optional) Which tab to file a document under. Argument is ignored if the `enqueue` parameter is set to true. |
| `subfolder` | string | no | (optional) Name of subfolder to file document under. While this is a freetext valie, it is strongly recommended that standardized subfolders be used in each top-level folder to avoid creating large numbers of distict subfolders. |
| `flag` | boolean | no | (optional) Set to true if this is a "key document" that will be accessibe on the first document tab of the patient dashboard |
| `requires_review` | number | no | (optional) If set, the id of the provider who needs to review this document. Must be a non-deleted user ID or -1 if it should be assigned to all provider tasks lists |
| `dr_reviewer` | number | no | (optional) If set, the id of the provider who signed off/reviewed this document. Set only if the document has been marked as reviewed |
| `dr_review_date` | date | no | (optional) If `dr_reviewer` is set, the date/time when the provider reviewed the document |
| `review_status` | number | no | (optional) If the document still needs review by user specified by `requires_review`, set to 1 |
| `result_code` | number | no | (optional) If a document is known too represent abnormal findings for the patient, you can flag it as borderline or abnormal, which changes the way the document displays. Values: 0 = Normal, 1 = Borderline, 2 = Abnormal |
| `follow_up_required_date` | date | no | (optional) The datetime that the system should notify clinician to re-review or follow up on document (creates a review task on this date) |
| `pt_notified` | number | no | (optional) Specify whether the patient has already been notified about the contents of this document. Values: 1 = Notification not needed, 2 = Patient has been notified |
| `pt_notified_method` | string | no | (optional) If `pt_notified` is set to '2' (patient has been notified), you can specify how they were notified. You can submit any string <155 characters but we recommend specifying from this list where appropriate |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `POST /patients/:patient_id/documents` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-patient-document.md) for the provider-specific parameters and requirements.

