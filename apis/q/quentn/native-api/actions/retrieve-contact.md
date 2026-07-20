# Retrieve Contact with Quentn

## Endpoint

- **Method:** `GET`
- **Path:** `/contact/:contact_id`
- **Base URL:** `https://tbg6y3.us-1.quentn.com/public/api/v1`
- **Official documentation:** [Retrieve Contact](https://help.quentn.com/hc/en-150/articles/4517835330961-Contact-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `number` | yes | The numeric Quentn contact ID to retrieve. This must be an existing contact id, not an email address. |
