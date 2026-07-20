# Create Assembly with Transloadit

Creates a new assembly in Transloadit.

## Endpoint

- **Method:** `POST`
- **Path:** `/assemblies`
- **Base URL:** `https://api2.transloadit.com`
- **Official documentation:** [Create Assembly](https://transloadit.com/docs/api/assemblies-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params` | body | `string` | yes | JSON string containing the Transloadit Assembly instructions, including steps and optional fields such as auth, template_id, notify_url, and signatures when applicable. |
