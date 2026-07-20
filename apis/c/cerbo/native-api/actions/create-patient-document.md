# Create Patient Document with Cerbo

Creates a new patient document in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/patients/:patient_id/documents`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Create Patient Document](https://docs.cer.bo/#tag/Patient-Documents/operation/createPatientDocument)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient |
| `enqueue` | query | `boolean` | no | (true by default) If true, the system will insert the document into the active patient portal queue so that the clinic is notified and can review the proposed addition |
| `pt_id` | body | `number` | no | (required) An integer identifier for the patient associated with the document. |
| `mime_type` | body | `string` | no | (required) A string indicating the MIME type of the file. |
| `name` | body | `string` | no | (required) A string to be used as the title of the document. |
| `base64_content` | body | `string` | no | (required) Binary data, encoded base64. Maximum file size is 16MB. |
| `notes` | body | `string` | no | (optional, enqueue=true only) A string to provide highlights or context about the document submission request when document is being enqueued (if accepted from the queue, this will get added to the document `content` section) |
| `content` | body | `string` | no | (optional, enqueue=false only) A string to provide highlights or context about the document when document is being injected directly into the patient chart (enqueue=false) |
| `folder` | body | `string` | no | (optional) Which tab to file a document under. Argument is ignored if the `enqueue` parameter is set to true. |
| `subfolder` | body | `string` | no | (optional) Name of subfolder to file document under. While this is a freetext valie, it is strongly recommended that standardized subfolders be used in each top-level folder to avoid creating large numbers of distict subfolders. |
| `flag` | body | `boolean` | no | (optional) Set to true if this is a "key document" that will be accessibe on the first document tab of the patient dashboard |
| `requires_review` | body | `number` | no | (optional) If set, the id of the provider who needs to review this document. Must be a non-deleted user ID or -1 if it should be assigned to all provider tasks lists |
| `dr_reviewer` | body | `number` | no | (optional) If set, the id of the provider who signed off/reviewed this document. Set only if the document has been marked as reviewed |
| `dr_review_date` | body | `date` | no | (optional) If `dr_reviewer` is set, the date/time when the provider reviewed the document |
| `review_status` | body | `number` | no | (optional) If the document still needs review by user specified by `requires_review`, set to 1 |
| `result_code` | body | `number` | no | (optional) If a document is known too represent abnormal findings for the patient, you can flag it as borderline or abnormal, which changes the way the document displays. Values: 0 = Normal, 1 = Borderline, 2 = Abnormal |
| `follow_up_required_date` | body | `date` | no | (optional) The datetime that the system should notify clinician to re-review or follow up on document (creates a review task on this date) |
| `pt_notified` | body | `number` | no | (optional) Specify whether the patient has already been notified about the contents of this document. Values: 1 = Notification not needed, 2 = Patient has been notified |
| `pt_notified_method` | body | `string` | no | (optional) If `pt_notified` is set to '2' (patient has been notified), you can specify how they were notified. You can submit any string <155 characters but we recommend specifying from this list where appropriate |
