# Count Future Appointments with HIPAAtizer

Retrieves the count of future appointments in HIPAAtizer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/api_key/appointments/count_future`
- **Base URL:** `https://app.hipaatizer.com`
- **Official documentation:** [Count Future Appointments](https://github.com/HIPAAtizer/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `object` | no | Optional raw request wrapper. Use `{}` when running without filters. |
| `request.locationIds` | body | `list<string>` | no | Optional location UUID filters. |
