# Create Message with Reamaze

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/:slug/messages`
- **Base URL:** `https://{brand}.reamaze.io/api/v1`
- **Official documentation:** [Create Message](https://www.reamaze.com/api/post_messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Path parameter for slug. |
| `message` | body | `object` | yes | Body payload field documented on https://www.reamaze.com/api/post_messages. |
