# Track an SMS with Routee

Tracks an SMS message in Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/sms/tracking/single/:trackingId`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Track an SMS](https://docs.routee.net/reference/smstrackingsingle)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trackingId` | path | `string` | yes | The unique tracking id of the sms |
