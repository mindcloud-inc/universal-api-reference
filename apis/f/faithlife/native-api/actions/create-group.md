# Create Group with Faithlife

Creates a new group in Faithlife.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups`
- **Base URL:** `https://accountsapi.logos.com/v2`
- **Official documentation:** [Create Group](https://developer.faithlife.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name for the new group. |
| `privacy` | body | `string` | yes | The group privacy setting. |
