# Unsubscribe contact from the defined mailing list with Routee

Unsubscribes a contact from a Routee mailing list.

## Endpoint

- **Method:** `GET`
- **Path:** `/addressbooks/:id/emails/unsubscribe`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Unsubscribe contact from the defined mailing list](https://docs.routee.net/reference/unsubscribe-contact-from-the-defined-mailing-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | the ID of the mailing list |
| `emails` | query | `string` | yes | contact, which you want to unsubscribe from defined mailing list ["example@yourdomain.com"] |
