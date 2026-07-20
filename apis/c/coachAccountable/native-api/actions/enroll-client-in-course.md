# Enroll Client in Course with CoachAccountable

Enrolls a client in a CoachAccountable course.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Enroll Client in Course](https://www.coachaccountable.com/APIDocs#Course.addClientParticipant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | The ID of the Client to be added. |
| `CourseID` | body | `number` | yes | The ID of the Course to which the Client is to be added. |
| `startDate` | body | `date` | no | A [future] date at which the Client is to start the Course. If not supplied (or not in the future) the Client will start the Course immediately. |
| `startOnDay` | body | `number` | no | Assuming an immediate start, you can supply startOnDay to jump a participant to some other Day in the Course [other than the usual Day 1 start]. |
| `dispatchEarlierStartDayItems` | body | `boolean` | no | Assuming an immediate start, you can have or skip items from the start day in the Course be dispatched (e.g. a Message set to go out at 9am if the Client is starting at 11am: should they get that message?). |
