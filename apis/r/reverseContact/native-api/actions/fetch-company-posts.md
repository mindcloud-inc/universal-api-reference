# Fetch Company Posts with Reverse Contact

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/fetch/companies/posts/live`
- **Base URL:** `https://api.reversecontact.com`
- **Official documentation:** [Fetch Company Posts](https://app.reversecontact.com/docs/endpoints/live-company-posts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public Social company URL whose posts should be fetched. |
| `webhookUrl` | body | `string` | no | HTTPS callback URL for live results. |
