# Get Submission by Hash with Peggy Pay

Retrieves a submission from Peggy Pay by submission hash.

## Endpoint

- **Method:** `GET`
- **Path:** `Formbuilder.Submissions.getSubmissionByHash`
- **Base URL:** `https://www.peggypay.com/api`
- **Official documentation:** [Get Submission by Hash](https://github.com/peggyforms/php-sdk/blob/master/src/Modules/Submissions.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | yes | Submission hash (`peggyHash`) from a Peggy Pay redirect or webhook. |
