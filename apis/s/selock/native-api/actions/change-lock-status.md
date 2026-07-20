# Change Lock Status with Selock

## Endpoint

- **Method:** `POST`
- **Path:** `/zaiper/change_lock_status/`
- **Base URL:** `https://selock.co/api/v1`
- **Official documentation:** [Change Lock Status](https://selock.co/en/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | body | `string` | yes | Target lock status, for example open or close. |
| `lock_id` | body | `string` | yes | Sciener lock identifier. |
