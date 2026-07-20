# Create Contact with Fleetio

Creates a new contact in Fleetio.

## Endpoint

- **Method:** `POST`
- **Path:** `contacts`
- **Base URL:** `https://secure.fleetio.com/api/`
- **Official documentation:** [Create Contact](https://developer.fleetio.com/docs/api/contacts-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Partner-Token` | header | `string` | no | — |
| `Organization-Token` | header | `string` | no | — |
| `first_name` | body | `string` | yes | This Contact's first name. |
| `middle_name` | body | `string` | no | This Contact's middle name. |
| `last_name` | body | `string` | no | This Contact's last name. |
| `birth_date` | body | `date` | no | This Contact's birth date. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `group_hierarchy` | body | `string` | no | If this Contact belongs to a [Group](/docs/api/groups), this will be a pipe delimited string representing the Group hierarchy. Each Group in the list is the parent of the `Groups` which follow. |
| `email` | body | `string` | no | This Contact's email address. |
| `mobile_phone_number` | body | `string` | no | This Contact's mobile phone number. |
| `home_phone_number` | body | `string` | no | This Contact's home phone number. |
| `work_phone_number` | body | `string` | no | This Contact's work phone number. |
| `other_phone_number` | body | `string` | no | Any other phone number for this Contact. |
| `street_address` | body | `string` | no | The street address of this Contact. |
| `street_address_line_2` | body | `string` | no | The second line of this Contact's street address. |
| `city` | body | `string` | no | The city of this Contact's address. |
| `region` | body | `string` | no | The region, state, province, or territory of this Contact's address. |
| `postal_code` | body | `string` | no | The postal code for this Contact's address. |
| `country` | body | `string` | no | The country where this Contact resides. |
| `employee_number` | body | `string` | no | This Contact's employee number. Must be unique. |
| `job_title` | body | `string` | no | This Contact's job title. |
| `start_date` | body | `date` | no | The date at which this Contact started, or is expected to start. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `leave_date` | body | `date` | no | The date at which this Contact left, or is expected to leave. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `vehicle_operator` | body | `boolean` | no | Whether this Contact is a Vehicle Operator. |
| `license_number` | body | `string` | no | The license number of this Contact. |
| `license_class` | body | `string` | no | The class of this Contact's license. |
| `license_state` | body | `string` | no | The state, province, region, or territory of this Contact's license. |
| `hourly_labor_rate` | body | `number` | no | The hourly labor rate for this Contact. |
| `custom_fields` | body | `object` | no | *Full details on working with Custom Fields [here](/docs/overview/custom-fields). |
| `group_id` | body | `number` | no | — |
| `license_expiration` | body | `date` | no | The date and time at which this Contact's license expires. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `employee` | body | `boolean` | no | Whether this Contact is an Employee. |
| `technician` | body | `boolean` | no | Whether this Contact is a Technician. |
| `user_access` | body | `boolean` | no | Whether this Contact has User Access. This must be set to true if using `account_membership_attributes`. |
| `account_membership_attributes` | body | `object` | no | These attributes require an Organization Token or Partner Token to be present in the request. Any role or record set attributes will be ignored if `user_type` is `admin`. `admin_role_attributes` will be ignored if `user_type` is not  `admin`. |
| `default_image_attributes` | body | `object` | no | — |
