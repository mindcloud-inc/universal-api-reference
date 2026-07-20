# Update a Person with Beebole

Updates an existing person in Beebole.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://beebole-apps.com/api/v2`
- **Official documentation:** [Update a Person](https://beebole.com/help/api#update-a-person)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `person.id` | body | `number` | yes |
| `person.name` | body | `string` | no |
| `person.email` | body | `string` | no |
| `person.invite` | body | `boolean` | no |
| `person.userGroup` | body | `string` | no |
