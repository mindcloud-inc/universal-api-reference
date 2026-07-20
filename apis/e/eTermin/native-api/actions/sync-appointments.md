# Sync Appointments with eTermin

Retrieves appointment changes from eTermin using a sync token.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/appointmentsync`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [Sync Appointments](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/AppointmentSync/get_api_appointmentsync)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `synctoken` | query | `number` | yes | SyncToken. If you start the synchronization the first time, please use 1. eTermin will return a (new) SyncToken after each call. This value can be found in the header. Please use then the new SnycToken when you call the api function again. |
