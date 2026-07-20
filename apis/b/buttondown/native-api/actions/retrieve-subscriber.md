# Retrieve Subscriber with Buttondown

Retrieves a subscriber from Buttondown by ID or email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers/:id_or_email`
- **Base URL:** `https://api.buttondown.com/v1`
- **Official documentation:** [Retrieve Subscriber](https://docs.buttondown.com/api-subscribers-retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_or_email` | path | `string` | yes | Subscriber ID or email address. |
