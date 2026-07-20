# Create Appointment Type with Cerbo

Creates a new appointment type in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/appointment_types`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Create Appointment Type](https://docs.cer.bo/#tag/Appointment-Types/operation/createAppointmentType)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the appointment type. Must be unique and contain at least one letter or number. |
| `default_length` | body | `number` | yes | Default duration in minutes. Must be between 5 minutes and 12 hours (720 minutes). |
| `name_portal` | body | `string` | no | Name displayed on the patient portal. Defaults to the same value as name if not specified. |
| `color_hex` | body | `string` | no | Six-character hexadecimal color code (without #) for calendar display. A random color is assigned if not specified. |
| `description` | body | `string` | no | Internal description of the appointment type. |
| `allow_on_portal` | body | `boolean` | no | Whether patients can book this type via the portal. |
| `number_of_overlaps_to_allow` | body | `number` | no | Maximum concurrent appointments of this type allowed (for group appointments). |
| `portal_notice` | body | `string` | no | Notice displayed to patients when booking via portal. |
| `which_providers[]` | body | `array<number>` | no | Array of provider IDs who can have this appointment type. Use [0] for all providers. |
| `sort_order` | body | `number` | no | Display order in appointment type lists. |
| `telemedicine` | body | `boolean` | no | Whether this is a telemedicine appointment type. |
| `email_notice_on` | body | `boolean` | no | Send email notification when appointment is created. |
| `email_notice` | body | `string` | no | Email body for appointment creation notification. |
| `email_notice_subject` | body | `string` | no | Subject line for appointment creation email. |
| `email_reminder_on` | body | `boolean` | no | Send automated email reminder before appointment. |
| `email_reminder` | body | `string` | no | Email body for reminder. |
| `email_reminder_subject` | body | `string` | no | Subject line for reminder email. |
| `email_reminder_hrs_before` | body | `number` | no | Hours before appointment to send email reminder (1 hour to 30 days). |
| `sms_reminder_on` | body | `boolean` | no | Send automated SMS reminder before appointment. |
| `sms_reminder` | body | `string` | no | SMS message text for reminder (max 220 characters). |
| `sms_reminder_hrs_before` | body | `number` | no | Hours before appointment to send SMS reminder (1 hour to 30 days). |
