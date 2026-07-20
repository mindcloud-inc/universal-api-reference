# Start Upload with Listclean

Starts a CSV upload in Listclean.

## Endpoint

- **Method:** `POST`
- **Path:** `/uploads/`
- **Base URL:** `https://api.listclean.xyz/v1`
- **Official documentation:** [Start Upload](https://api.listclean.xyz/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | yes | CSV file name. |
| `file_type` | body | `string` | yes | File type, for example csv. |
| `total_chunk_count` | body | `number` | yes | Total number of chunks for the upload. |
| `max_chunk_size` | body | `number` | yes | Maximum chunk size in bytes. |
| `email_column_index` | body | `number` | yes | Zero-based index of the CSV column that contains email addresses. Runtime required by Listclean even though the current OpenAPI request schema omits it. |
| `separator_char` | body | `string` | no | CSV separator character. |
| `enclosure_char` | body | `string` | no | Optional field enclosure character, one single-byte character only. |
| `escape_char` | body | `string` | no | Optional escape character. An empty value disables escaping. |
| `fast_process` | body | `number` | no | Set to 1 for faster processing that avoids slower operations such as SMTP validation; default is 0. |
