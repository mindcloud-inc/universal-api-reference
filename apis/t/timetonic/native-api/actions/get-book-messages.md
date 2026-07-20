# Get Book Messages with Timetonic

Retrieves messages for a book from Timetonic.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://timetonic.com/live/api.php`
- **Official documentation:** [Get Book Messages](https://timetonic.com/live/api.php?doc=#getBookMessages-doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `b_c` | body | `string` | yes | Book code to inspect. |
| `b_o` | body | `string` | yes | Book owner to inspect. |
| `sstamp` | body | `string` | no | Optional sync stamp for incremental reads. |
| `smidFirst` | body | `string` | no | Optional lower message-id bound. |
| `smidLast` | body | `string` | no | Optional upper message-id bound. |
| `nbMax` | body | `string` | no | Optional maximum number of messages to return. |
| `page` | body | `string` | no | Optional page number. |
| `search_string` | body | `string` | no | Optional free-text search string. |
