# Create Assignment with Innform

Assigns a training item to a user in Innform.

## Endpoint

- **Method:** `POST`
- **Path:** `/assignments`
- **Base URL:** `https://api.innform.io/v1`
- **Official documentation:** [Create Assignment](https://innform.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `due_date` | body | `date` | no | Optional assignment due date. |
| `item_id` | body | `string` | yes | Course or learning path UUID to assign. |
| `item_type` | body | `string` | no | Optional item type such as LearningPath. Accepted values: `0`. |
| `user_id` | body | `string` | yes | User UUID to assign. |
