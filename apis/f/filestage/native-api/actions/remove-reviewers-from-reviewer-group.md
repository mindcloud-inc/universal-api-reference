# Remove Reviewers from Reviewer Group with Filestage

Deletes reviewers from a Filestage reviewer group.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/steps/{stepId}/reviewer`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Remove Reviewers from Reviewer Group](https://developers.filestage.io/docs/api/1kssr3rtqap4w-remove-reviewers-from-reviewer-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reviewerId` | query | `string` | no | When the reviewerId is missing then the email parameter must be provided |
| `email` | query | `string` | no | Reviewer's email. |
| `stepId` | path | `string` | yes | Step Id |
