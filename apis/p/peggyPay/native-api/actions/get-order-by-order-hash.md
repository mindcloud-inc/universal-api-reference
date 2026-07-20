# Get Order by Order Hash with Peggy Pay

Retrieves an order from Peggy Pay by order hash.

## Endpoint

- **Method:** `GET`
- **Path:** `Formbuilder.Submissions.getOrder`
- **Base URL:** `https://www.peggypay.com/api`
- **Official documentation:** [Get Order by Order Hash](https://github.com/peggyforms/php-sdk/blob/master/src/Modules/Orders.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | yes | Peggy Pay order hash. |
