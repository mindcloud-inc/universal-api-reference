# Update Subscriber with Sendloop

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriber.update/json`
- **Base URL:** `https://{subdomain}.sendloop.com/api/v3`
- **Official documentation:** [Update Subscriber](https://chmyos.notion.site/Update-a-Subscriber-efc3bdade57e448cb862ce6924cad424)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ListID` | body | `number` | yes | ID of the target list |
| `SubscriberID` | body | `number` | yes | ID number of the target subscriber |
| `EmailAddress` | body | `string` | no | Email address of the subscriber |
