# Create Group with AMcards.com

Creates a new contact group in AMcards.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/group/`
- **Base URL:** `https://amcards.com/.api/v1`
- **Official documentation:** [Create Group](https://staging.amcards.com/docs/developers-only/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Name for the new contact group. |
| `owner` | body | `string` | no | AMcards owner resource URI such as `/.api/v1/user/47054/`. |
