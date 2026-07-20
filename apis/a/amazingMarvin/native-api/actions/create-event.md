# Create Event with Amazing Marvin

Creates an event in Amazing Marvin.

## Endpoint

- **Method:** `POST`
- **Path:** `/addEvent`
- **Base URL:** `https://serv.amazingmarvin.com/api`
- **Official documentation:** [Create Event](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#create-an-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Event title. |
| `start` | body | `string` | yes | ISO formatted start time. |
| `length` | body | `number` | yes | Event length in milliseconds. |
| `note` | body | `string` | no | Optional event note in markdown. |
