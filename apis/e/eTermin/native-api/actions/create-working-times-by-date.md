# Create Working Times by Date with eTermin

Creates working times by date in eTermin.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/workingtimesdate`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [Create Working Times by Date](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/WorkingTimesDate/post_api_workingtimesdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `string` | yes | Start date/time of working time e.g. 2019-07-14 09:00 |
| `end` | query | `string` | yes | End date/time of working time e.g. 2019-07-14 18:00 |
| `calendarid` | query | `number` | yes | ID of the calendar |
| `reason` | query | `string` | no | Reason of the specific working time (this is only visible internally) |
| `slottype` | query | `number` | no | 0 if time slots should be valid for internal and external (online booked) appointments. 1 if timeslots are only valid for interal (manually entered) appointments |
| `nrapps` | query | `number` | no | Amount of appointments that are bookable in this working slot. (-1 = unlimited) |
| `overwriteday` | query | `boolean` | no | true, if the workingtime for this day should be disabled |
| `validwithserviceid` | query | `string` | no | List of services that work with this working slot |
| `allserviceidsrequired` | query | `number` | no | Defines how the validity of the services are checked. Exclusive means that only the services provided with the parameter validwithserviceid are allowed. If not exclusive, every service the calendar is activated for can be used. <br> 0 = one service needs to be selected <br> 1 = all services need to be selected exclusively <br> 2 = all services need to be selected <br> 3 = one service needs to be selected exclusively) |
| `locationid` | query | `number` | no | ID of the location for this working slot if locations are used in working times |
| `oneoff` | query | `boolean` | no | true, if this timeslot needs a specific link (requires exactly one service for the validwithserviceid parameter) |
| `oneoffcode` | query | `string` | no | Specific code that is used for the oneoff-link if oneoff is true |
| `waitinglist` | query | `boolean` | no | true, if this timeslot should be filled with appointments from the waitinglist |
