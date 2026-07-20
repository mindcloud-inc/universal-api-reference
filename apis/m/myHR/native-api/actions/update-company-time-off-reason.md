# Update Company Time Off Reason with MyHR

## Endpoint

- **Method:** `PUT`
- **Path:** `/company_timeoff_reasons/:company_timeoff_reason_pid`
- **Base URL:** `https://mindcloud.myhr.lu/api/v2`
- **Official documentation:** [Update Company Time Off Reason](https://www.postman.com/myhr-api/request/27799381-230f8f8b-2eff-4b54-a5dd-3b7a783a5ca4)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_timeoff_reason_pid` | path | `string` | yes | The company time off reason PID. |
| `label` | body | `string` | yes | The updated company time off reason label. |
