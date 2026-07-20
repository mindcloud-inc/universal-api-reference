# Create Subscription with Billwerkplus

Creates a subscription in Billwerkplus.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscription`
- **Base URL:** `https://api.frisbii.com/v1`
- **Official documentation:** [Create Subscription](https://docs.frisbii.com/reference/createsubscriptionjson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer` | body | `string` | yes | Existing customer handle. |
| `plan` | body | `string` | yes | Plan handle. |
| `handle` | body | `string` | yes | Unique subscription handle. |
| `signup_method` | body | `string` | yes | How the customer provides payment information. |
| `test` | body | `boolean` | no | Create the subscription in test mode. |
| `show_terms` | body | `boolean` | no | Show terms of service on the signup page. |
| `start_date` | body | `string` | no | Future start date for the subscription. |
