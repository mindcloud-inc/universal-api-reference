# Add Suppressed Domain with Retently

Creates a suppressed domain entry in Retently.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/suppressions/domains`
- **Base URL:** `https://app.retently.com`
- **Official documentation:** [Add Suppressed Domain](https://www.retently.com/api/#api-post-suppressions-domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pattern` | body | `string` | yes | The domain pattern to suppress. Supports wildcards (e.g., *.example.com); |
| `category` | body | `string` | no | Category of the domain. Values: other (default), corporate, disposable, invalid; |
| `note` | body | `string` | no | An optional note explaining why the domain was suppressed; |
