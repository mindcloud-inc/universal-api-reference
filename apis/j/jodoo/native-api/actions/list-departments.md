# List Departments with Jodoo

## Endpoint

- **Method:** `POST`
- **Path:** `/corp/department/list`
- **Base URL:** `https://api.jodoo.com/api/v5`
- **Official documentation:** [List Departments](https://help.jodoo.com/en/articles/9992464-department-lists-retrieval-recursively)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dept_no` | body | `number` | yes | Department number to retrieve child departments from recursively. |
