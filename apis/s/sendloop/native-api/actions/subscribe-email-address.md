# Subscribe Email Address with Sendloop

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriber.subscribe/json`
- **Base URL:** `https://{subdomain}.sendloop.com/api/v3`
- **Official documentation:** [Subscribe Email Address](https://chmyos.notion.site/Subscribe-an-Email-Address-24b06739a31c42a199d8888984bb7b1b)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EmailAddress` | body | `string` | yes | The email address which is going to be subscribed |
| `ListID` | body | `number` | yes | ID of the target subscriber list |
| `SubscriptionIP` | body | `string` | no | IP address of the subscriber |
