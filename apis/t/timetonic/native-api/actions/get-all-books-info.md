# Get All Books Info with Timetonic

Retrieves information for all books from Timetonic.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://timetonic.com/live/api.php`
- **Official documentation:** [Get All Books Info](https://timetonic.com/live/api.php?doc=#getAllBooks-doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sstamp` | body | `string` | no | Optional sync stamp for incremental reads. |
| `b_c` | body | `string` | no | Optional book code to narrow the response. |
| `b_o` | body | `string` | no | Optional book owner to narrow the response. |
