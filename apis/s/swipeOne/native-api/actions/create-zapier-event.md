# Create Zapier Event with Swipe One

## Endpoint

- **Method:** `POST`
- **Path:** `/zapier/event`
- **Base URL:** `https://api.swipeone.com/api`
- **Official documentation:** [Create Zapier Event](https://docs.swipeone.com/en/articles/10420029-swipeone-apis#h_6c762d18ff)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `string` | yes | The name of the event to create. |
| `contact` | body | `string` | yes | The contact identifier, either an email address or phone number. |
