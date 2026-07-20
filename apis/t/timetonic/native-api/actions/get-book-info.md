# Get Book Info with Timetonic

Retrieves information for a book from Timetonic.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://timetonic.com/live/api.php`
- **Official documentation:** [Get Book Info](https://timetonic.com/live/api.php?doc=#getBookInfo-doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sstamp` | body | `string` | no | Optional sync stamp for incremental reads. |
| `b_c` | body | `string` | yes | Book code to inspect. |
| `b_o` | body | `string` | yes | Book owner to inspect. |
