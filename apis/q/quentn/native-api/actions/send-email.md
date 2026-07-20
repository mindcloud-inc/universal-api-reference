# Send Email with Quentn

## Endpoint

- **Method:** `POST`
- **Path:** `/mail/:email_id/send`
- **Base URL:** `https://tbg6y3.us-1.quentn.com/public/api/v1`
- **Official documentation:** [Send Email](https://help.quentn.com/hc/en-150/articles/4518209942289-Mail-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_id` | path | `number` | yes | The numeric Quentn email id to send. |
| `recipients[0].id` | body | `number` | yes | Single recipient contact id for the email send request. |
| `sender_id` | body | `number` | no | Optional sender id to use when sending the email. |
