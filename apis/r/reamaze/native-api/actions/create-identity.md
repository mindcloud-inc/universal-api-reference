# Create Identity with Reamaze

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:email/identities`
- **Base URL:** `https://{brand}.reamaze.io/api/v1`
- **Official documentation:** [Create Identity](https://www.reamaze.com/api/post_identities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Path parameter for email. |
| `identity` | body | `object` | yes | Body payload field documented on https://www.reamaze.com/api/post_identities. |
