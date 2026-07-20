# Create Labels with Routee

Creates new contact labels in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/labels/my`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Create Labels](https://docs.routee.net/reference/create-labels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of label. May only contain alphanumeric characters. |
| `type` | body | `string` | no | The type of label (Text, Number) |
