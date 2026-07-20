# Sending Text Message with Mention with Picky Assist

## Endpoint

- **Method:** `POST`
- **Path:** `/push`
- **Base URL:** `https://app.pickyassist.com/api/v2`
- **Official documentation:** [Sending Text Message with Mention](https://help.pickyassist.com/api-documentation-v2/postman-collection-for-picky-assist-apis)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `application` | body | `string` | yes |
| `group_id` | body | `string` | yes |
| `globalmessage` | body | `string` | yes |
