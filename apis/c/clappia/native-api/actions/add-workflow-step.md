# Add Workflow Step with Clappia

Creates a new workflow step in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflowdefinitionv2/addWorkflowStep`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Add Workflow Step](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `triggerType` | body | `string` | yes | Workflow trigger type, such as newSubmission, editSubmission, or reviewSubmission. |
| `nodeType` | body | `string` | yes | Workflow node type, such as email, wait, condition, sms, approval, restApi, or ai. |
| `parentVariableName` | body | `string` | yes | Parent workflow step variable name under which the new step should be attached. |
| `toEmailAddresses[]` | body | `array<string>` | no | Recipient email addresses for email nodes. |
| `ccEmailAddresses[]` | body | `array<string>` | no | CC email addresses for email nodes. |
| `bccEmailAddresses[]` | body | `array<string>` | no | BCC email addresses for email nodes. |
| `subject` | body | `string` | no | Message subject for email or notification nodes. |
| `body` | body | `string` | no | Message or template body for the workflow step. |
| `replyTo` | body | `string` | no | Reply-to email address for email nodes. |
| `staticAttachments[]` | body | `array<object>` | no | Static attachment objects for supported workflow nodes. |
| `printTemplateIndices[]` | body | `array<number>` | no | Print template indices to attach for supported nodes. |
| `dynamicAttachments[]` | body | `array<string>` | no | Field names whose files should be attached dynamically. |
