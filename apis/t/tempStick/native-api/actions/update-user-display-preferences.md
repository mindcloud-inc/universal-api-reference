# Update User Display Preferences with Temp Stick

Updates Temp Stick display preferences for the current user.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/display-preferences`
- **Base URL:** `https://tempstickapi.com/api/v1`
- **Official documentation:** [Update User Display Preferences](https://tempstickapi.com/docs/#api-User-Update_User_Display_Preferences)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timezone` | body | `string` | yes | Time zone of the user, functionally used in determining if an alert should trigger if a time window is set |
| `temp_pref` | body | `string` | yes | Display alerts in fahrenheit or celsius |
| `chart_fill` | body | `number` | no | Set whether to have the chart normalized on the Y-axis |
