# Update Working Times with eTermin

Updates existing working times in eTermin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/workingtimes`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [Update Working Times](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/WorkingTimes/put_api_workingtimes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | yes | ID of the working time that needs to be changed |
| `start` | query | `string` | no | Start time of the slot, e.g. 09:00 |
| `end` | query | `string` | no | End time of the slot, e.g. 17:00 |
| `calendarid` | query | `number` | no | ID of the calendar |
| `weekday` | query | `string` | no | ID of the weekday 1 = Sunday, 7 = Saturday. You can add several weekdays separated by a comma e.g. 2,3,5 |
| `enable` | query | `number` | no | 0 if the time slot should exist but not being considered yet |
| `slottype` | query | `number` | no | 0 if time slots should be valid for internal and external (online booked) appointments. 1 if timeslots are only valid for interal (manually entered) appointments |
| `validwithserviceid` | query | `string` | no | List of services that work with this working slot |
| `allserviceidsrequired` | query | `number` | no | Defines how the validity of the services are checked. Exclusive means that only the services provided with the parameter validwithserviceid are allowed. If not exclusive, every service the calendar is activated for can be used. <br> 0 = one service needs to be selected <br> 1 = all services need to be selected exclusively <br> 2 = all services need to be selected <br> 3 = one service needs to be selected exclusively) |
| `nrapps` | query | `number` | no | Amount of appointments that are bookable in this working slot. (-1 = unlimited) |
| `weektype` | query | `number` | no | Defines in which interval the time slot should be shown <br> 0 = Every week <br> 1 = Odd weeks <br> 2 = Even weeks <br> 3 = First occurrence in month <br> 4 = second occurrence in month <br> 5 = third occurrence in month <br> 6 = fourth occurrence in month <br> 7 = Every 3 weeks first occurrence <br> 8 = Every 3 weeks second occurrence <br> 9 = Every 3 weeks third occurrence <br> 10 = fifth occurrence in month <br> 11 = Every 4 weeks first occurrence <br> 12 = Every 4 weeks second occurrence <br> 13 = Every 4 weeks third occurrence <br> 14 = Every 4 weeks fourth occurrence |
| `locationid` | query | `number` | no | ID of the location for this working slot if locations are used in working times |
| `calendarintervalid` | query | `number` | no | ID of the period for this working slot if periods are used in working times |
