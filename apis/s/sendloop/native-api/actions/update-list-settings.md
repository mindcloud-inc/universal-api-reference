# Update List Settings with Sendloop

## Endpoint

- **Method:** `POST`
- **Path:** `/list.settings.update/json`
- **Base URL:** `https://{subdomain}.sendloop.com/api/v3`
- **Official documentation:** [Update List Settings](https://chmyos.notion.site/Update-List-Settings-0deb49bea02d43c6a27779648ecaa3e3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ListID` | body | `number` | yes | ID number of the target subscriber list |
| `SubscriptionFinalAction` | body | `string` | no | Pass Nothing or Send Email |
