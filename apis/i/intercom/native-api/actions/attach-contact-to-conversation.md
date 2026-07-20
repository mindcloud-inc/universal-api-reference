# Attach Contact To Conversation with Intercom

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/:conversation_id/customers`
- **Base URL:** `https://api.intercom.io`
- **Official documentation:** [Attach Contact To Conversation](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/conversations/attachcontacttoconversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Intercom conversation identifier |
| `admin_id` | body | `string` | yes | Admin performing the action |
| `customer` | body | `object` | no | — |
| `customer.intercom_user_id` | body | `string` | no | Intercom contact ID to attach as a customer |
| `customer.user_id` | body | `string` | no | Alternative provider user_id for customer identification |
| `customer.email` | body | `string` | no | Alternative customer email for identification |
