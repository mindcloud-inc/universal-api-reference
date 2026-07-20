# Get Order by Submission Hash with Peggy Pay

Retrieves an order from Peggy Pay by submission hash.

## Endpoint

- **Method:** `GET`
- **Path:** `Formbuilder.Submissions.getOrder`
- **Base URL:** `https://www.peggypay.com/api`
- **Official documentation:** [Get Order by Submission Hash](https://github.com/peggyforms/php-sdk/blob/master/src/Modules/Orders.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | yes | Submission hash (`peggyHash`) from a Peggy Pay redirect or webhook. |
