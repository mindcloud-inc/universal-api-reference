# Update Response Status with HRBLADE

## Endpoint

- **Method:** `POST`
- **Path:** `/response/change/status`
- **Base URL:** `https://api.hrblade.com/api`
- **Official documentation:** [Update Response Status](https://documenter.getpostman.com/view/15055534/TzCFgWPB)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `response_id` | body | `number` | yes | Response identifier. |
| `status` | body | `string` | yes | Status value. |
