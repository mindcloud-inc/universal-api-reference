# Get User with Rocketlane

Retrieves a user from Rocketlane.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.0/users/:userId`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [Get User](https://developer.rocketlane.com/reference/get-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `number` | yes | The user's unique, system-generated identifier, which can be used to identify the user globally. |
| `includeFields` | query | `list<string>` | no | This query parameter allows you to specify which fields should be returned in the response body by selecting from the drop down. To get the relevant fields, use comma separated values. If the field is left blank, the default properties are returned. |
| `includeAllFields` | query | `boolean` | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
