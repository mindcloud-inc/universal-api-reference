# Create Install Ticket with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `CreateTemplateAppInstallTicket`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Create Install Ticket](https://learn.microsoft.com/en-us/rest/api/power-bi/template-apps/create-install-ticket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `installDetails[]` | body | `array<object>` | no | List of install details |
