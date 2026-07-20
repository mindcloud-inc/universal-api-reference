# Update Student Custom Field with Xperiencify

Updates a student custom field in Xperiencify.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/student/customfield/`
- **Base URL:** `https://api.xperiencify.io`
- **Official documentation:** [Update Student Custom Field](https://intercom.help/xperiencify/en/articles/9888509-integrating-with-the-api#h_a27eec35e6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `student` | body | `string` | yes | Student email address. |
| `field` | body | `string` | yes | Custom field name. |
| `value` | body | `string` | yes | Custom field value. |
