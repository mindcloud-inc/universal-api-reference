# Create Or Update Business Trip with GIRITON

Creates or updates a business trip in GIRITON.

## Endpoint

- **Method:** `POST`
- **Path:** `/attendance/businessTrip`
- **Base URL:** `https://rest.giriton.com/system/api`
- **Official documentation:** [Create Or Update Business Trip](https://rest.giriton.com/apidoc/#/Attendance/addUpdateBusinessTrip)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `person.id` | body | `string` | yes | Person ID nested under the GIRITON person request object. |
| `dateTimeFrom` | body | `string` | yes | Business trip start date and time in GIRITON's documented ISO offset format. |
| `dateTimeTo` | body | `string` | yes | Business trip end date and time in GIRITON's documented ISO offset format. |
| `description` | body | `string` | no | Business trip description. |
| `distanceKm` | body | `number` | no | Business trip distance in kilometers. |
| `foreignTrip` | body | `boolean` | no | Whether the business trip is foreign. |
