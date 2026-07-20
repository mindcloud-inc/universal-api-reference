# Evaluate Task with Intradesk

Submits an evaluation for a task in Intradesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/changes/v3/Tasks/evaluate`
- **Base URL:** `https://apigw.intradesk.ru`
- **Official documentation:** [Evaluate Task](https://apigw.intradesk.ru/changes_docs/swagger/index.html#/Tasks/post_v3_Tasks_evaluate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | TaskEvaluationRequestModel JSON object request body documented by Intradesk Changes API. |
