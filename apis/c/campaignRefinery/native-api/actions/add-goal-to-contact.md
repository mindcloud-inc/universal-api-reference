# Add Goal to Contact with Campaign Refinery

Adds a goal to a contact in Campaign Refinery.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/add-goal`
- **Base URL:** `https://app.campaignrefinery.com/rest`
- **Official documentation:** [Add Goal to Contact](https://developers.campaignrefinery.com/reference/add-goal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The contact's ID. |
| `goal_id` | body | `string` | yes | The goal UUID. |
