# Bulk Update Events By Reference Type with ECAL

Updates ECAL events by reference type.

## Endpoint

- **Method:** `PUT`
- **Path:** `/events/:referenceType`
- **Base URL:** `https://api.ecal.com/apiv2`
- **Official documentation:** [Bulk Update Events By Reference Type](https://docs.ecal.com/reference/apiv2/event.html#put-apiv2eventsreferencetype)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `referenceType` | path | `string` | yes | Reference type used to bulk update matching events. |
| `requestBody` | body | `object` | yes | JSON object matching ECAL's bulk event update payload. |
