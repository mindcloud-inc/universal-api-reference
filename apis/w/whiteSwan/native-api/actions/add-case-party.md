# Add Case Party with White Swan

Adds a case party to a White Swan case.

## Endpoint

- **Method:** `POST`
- **Path:** `/invite_case_party`
- **Base URL:** `https://app.whiteswan.io/api/1.1/wf`
- **Official documentation:** [Add Case Party](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/action-calls/add-case-party)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `string` | yes | White Swan request ID to grant access to. |
| `invitee_email` | body | `string` | no | Email that should receive case access. |
| `invitee_phone` | body | `string` | no | Phone number that should receive case access. |
