# Get Employee By Foreign Key with MyHR

## Endpoint

- **Method:** `GET`
- **Path:** `/employees/@`
- **Base URL:** `https://mindcloud.myhr.lu/api/v2`
- **Official documentation:** [Get Employee By Foreign Key](https://www.postman.com/myhr-api/request/27799381-792e87f4-f1f6-4cf6-91d5-d1ef5e9c9564)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeForeignKey` | body | `string` | yes | Employee foreign key used to resolve the @ endpoint header. |
