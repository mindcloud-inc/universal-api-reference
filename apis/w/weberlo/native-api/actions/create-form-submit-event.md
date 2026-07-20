# Create Form Submit Event with Weberlo

Creates a form submit event in Weberlo.

## Endpoint

- **Method:** `POST`
- **Path:** `/event/form`
- **Base URL:** `https://connect.weberlo.com`
- **Official documentation:** [Create Form Submit Event](https://developers.weberlo.com/#tag/Event/paths/~1event~1form/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `time` | body | `number` | yes | Event timestamp in milliseconds. |
| `email` | body | `string` | no | Visitor email address. |
| `first_name` | body | `string` | no | Visitor first name. |
| `last_name` | body | `string` | no | Visitor last name. |
| `name` | body | `string` | no | Visitor full name. |
| `form_type` | body | `string` | no | Form type label. |
| `form_id` | body | `string` | no | Form identifier. |
| `session_id` | body | `string` | no | Session identifier. |
| `website` | body | `string` | no | Website host or name. |
| `href` | body | `string` | no | Page URL where the form submit happened. |
| `device` | body | `string` | no | Device type. |
| `country` | body | `string` | no | Country code or country value. |
| `phone` | body | `string` | no | Visitor phone number. |
| `ip_address` | body | `string` | no | Visitor IP address. |
| `utm_source` | body | `string` | no | UTM source. |
| `utm_medium` | body | `string` | no | UTM medium. |
| `utm_campaign` | body | `string` | no | UTM campaign. |
| `utm_content` | body | `string` | no | UTM content. |
| `fbclid` | body | `string` | no | Facebook click identifier. |
| `gclid` | body | `string` | no | Google click identifier. |
