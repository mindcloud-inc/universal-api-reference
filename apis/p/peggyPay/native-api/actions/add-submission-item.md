# Add Submission Item with Peggy Pay

Updates a Peggy Pay submission by adding an item.

## Endpoint

- **Method:** `GET`
- **Path:** `Formbuilder.Submissions.addItem`
- **Base URL:** `https://www.peggypay.com/api`
- **Official documentation:** [Add Submission Item](https://github.com/peggyforms/php-sdk/blob/master/src/Modules/Submissions.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | yes | Submission hash to update. |
| `item[key]` | query | `string` | yes | Unique item key; existing keys are overwritten by Peggy Pay. |
| `item[label]` | query | `string` | yes | Human-readable item label. |
| `item[value]` | query | `string` | yes | Item value to store on the submission. |
