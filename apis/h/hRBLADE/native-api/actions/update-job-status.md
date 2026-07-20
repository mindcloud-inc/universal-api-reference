# Update Job Status with HRBLADE

## Endpoint

- **Method:** `POST`
- **Path:** `/job/active`
- **Base URL:** `https://api.hrblade.com/api`
- **Official documentation:** [Update Job Status](https://documenter.getpostman.com/view/15055534/TzCFgWPB)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | yes | Active status flag. |
| `job_id` | body | `number` | yes | Job identifier. |
