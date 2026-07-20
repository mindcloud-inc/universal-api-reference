# Log Task Expense with Intradesk

Logs a task expense in Intradesk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/changes/v1/TaskExpenses`
- **Base URL:** `https://apigw.intradesk.ru`
- **Official documentation:** [Log Task Expense](https://apigw.intradesk.ru/changes_docs/swagger/index.html#/TaskExpenses/put_v1_TaskExpenses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | TaskExpensesRequestModel JSON object request body documented by Intradesk Changes API. |
