# Add Numbers to Group with Sempico Solutions SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/group-number-add`
- **Base URL:** `https://restapi.sempico.solutions/v1`
- **Official documentation:** [Add Numbers to Group](https://pypi.org/pypi/gatum-rest-py/json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_group` | body | `number` | yes | Group ID to add numbers to. |
| `numbers[]` | body | `array<object>` | yes | Numbers to add to the group. Each item can include number plus optional name, surname, patronymic, date_birth, male, and note_1 through note_10 fields. |
