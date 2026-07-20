# Temp Stick: Native API Reference

A consolidated summary of Temp Stick's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://tempstickapi.com/docs/
- **API base URL:** `https://tempstickapi.com/api/v1`

## Authentication

### API Key

Authenticate with your Temp Stick API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://tempstickapi.com/docs/)

## API conventions

Responses from this API use JSON.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Alert](actions/get-alert.md) | `GET /alerts/:alert_id` | [docs](https://tempstickapi.com/docs/#api-Alerts-Get_Alert) |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://tempstickapi.com/docs/#api-User-Get_Current_User) |
| [Get Email Reports](actions/get-email-reports.md) | `GET /user/email-reports` | [docs](https://tempstickapi.com/docs/#api-User-Get_Email_Reports) |
| [Get Sensor](actions/get-sensor.md) | `GET /sensor/:sensor_id` | [docs](https://tempstickapi.com/docs/#api-Sensors-Get_Sensor) |
| [Get Sensor Readings](actions/get-sensor-readings.md) | `GET /sensor/:sensor_id/readings` | [docs](https://tempstickapi.com/docs/#api-Sensors-Get_Sensor_Readings) |
| [List Alerts](actions/list-alerts.md) | `GET /alerts/all` | [docs](https://tempstickapi.com/docs/#api-Alerts-Get_Alerts) |
| [List Sensor Notifications](actions/list-sensor-notifications.md) | `GET /sensor/notifications/:sensorId` | [docs](https://tempstickapi.com/docs/#api-Alerts-Get_Sensor_Notifications) |
| [List Sensors](actions/list-sensors.md) | `GET /sensors/all` | [docs](https://tempstickapi.com/docs/#api-Sensors-Get_Sensors) |
| [List Timezones](actions/list-timezones.md) | `GET /user/allowed-timezones` | [docs](https://tempstickapi.com/docs/#api-User-Get_Timezones) |
| [List User Notifications](actions/list-user-notifications.md) | `GET /user/notifications` | [docs](https://tempstickapi.com/docs/#api-Alerts-Get_User_Notifications) |
| [Update Sensor Settings](actions/update-sensor-settings.md) | `POST /sensor/:sensor_id` | [docs](https://tempstickapi.com/docs/#api-Sensors-Update_Sensor_Settings) |
| [Update User Display Preferences](actions/update-user-display-preferences.md) | `POST /user/display-preferences` | [docs](https://tempstickapi.com/docs/#api-User-Update_User_Display_Preferences) |
