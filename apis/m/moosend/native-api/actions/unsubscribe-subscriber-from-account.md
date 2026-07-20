# Unsubscribe Subscriber From Account with Moosend

Unsubscribes a subscriber from a Moosend account.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/unsubscribe.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Unsubscribe Subscriber From Account](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54579-Unsubscribe-a-subscriber-from-an-account?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Email` | body | `string` | yes | The email address of the subscriber. |
