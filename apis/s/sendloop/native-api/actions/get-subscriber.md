# Get Subscriber with Sendloop

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriber.get/json`
- **Base URL:** `https://{subdomain}.sendloop.com/api/v3`
- **Official documentation:** [Get Subscriber](https://chmyos.notion.site/Get-a-Subscriber-2609e6e0fd7c4b0caa30da3cd6e13c15)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ListID` | body | `number` | yes | ID of the target list to get the subscriber from |
| `SubscriberID` | body | `number` | no | ID number of the target subscriber |
| `EmailAddress` | body | `string` | no | Email address of the subscriber |
