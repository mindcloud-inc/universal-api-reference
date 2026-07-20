# Set Review Due Date with Filestage

Sets a due date for a Filestage review.

## Endpoint

- **Method:** `PUT`
- **Path:** `/reviews/{reviewId}/due-date`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Set Review Due Date](https://developers.filestage.io/docs/api/4e8t7j93p6k0q-set-review-due-date)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reviewId` | path | `string` | yes | Review Id |
| `dueDate` | body | `date` | yes | — |
