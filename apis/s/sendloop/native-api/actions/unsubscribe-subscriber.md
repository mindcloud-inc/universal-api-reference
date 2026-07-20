# Unsubscribe Subscriber with Sendloop

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriber.unsubscribe/json`
- **Base URL:** `https://{subdomain}.sendloop.com/api/v3`
- **Official documentation:** [Unsubscribe Subscriber](https://chmyos.notion.site/Unsubscribe-a-Subscriber-39e13dd994fd48ce8f4da068f5ac39c9)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EmailAddress` | body | `string` | yes | The email address which is going to be unsubscribed |
| `ListID` | body | `number` | yes | Set the target list ID |
| `UnsubscriptionIP` | body | `string` | no | Pass 0.0.0.0 if you want to ignore this |
