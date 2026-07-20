# Create a Person with Beebole

Creates a new person in Beebole.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://beebole-apps.com/api/v2`
- **Official documentation:** [Create a Person](https://beebole.com/help/api#create-a-person)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `person.name` | body | `string` | yes |
| `person.company.id` | body | `number` | yes |
| `person.email` | body | `string` | no |
| `person.invite` | body | `boolean` | no |
| `person.userGroup` | body | `string` | no |
