# Merge Subscriber with Sequenzy

Creates or merges a subscriber in Sequenzy by email.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers`
- **Base URL:** `https://api.sequenzy.com/api/v1`
- **Official documentation:** [Merge Subscriber](https://docs.sequenzy.com/api-reference/subscribers/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Subscriber email address. |
